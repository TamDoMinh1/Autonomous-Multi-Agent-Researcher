# 🔬 Autonomous Multi-Agent Researcher

[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![Agentic-Workflow](https://img.shields.io/badge/Workflow-Agentic-orange.svg)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

The **Autonomous Multi-Agent Researcher** is a state-of-the-art framework that simulates a collaborative research environment. It leverages multiple specialized AI agents (Researcher, Critic, and Writer) to autonomously explore complex topics, verify information across sources, and synthesize high-quality technical reports.

## 🔄 The Collaborative Workflow

1. **Researcher Agent**: Performs deep-dive searches, extracts key data points, and gathers evidence.
2. **Critic Agent**: Evaluates the gathered information for accuracy, identifies gaps, and requests further research if necessary.
3. **Writer Agent**: Synthesizes verified findings into a structured, professional report (Markdown/PDF).
4. **Reflector Loop**: Iteratively refines the output based on internal peer review between agents.

## 🏗️ Architecture

`mermaid
graph TD
    Goal([Research Topic]) --> Orchestrator{Agent Orchestrator}
    Orchestrator --> Researcher[Researcher Agent]
    Researcher --> Search[(External Knowledge)]
    Researcher --> Data[Raw Research Data]
    Data --> Critic[Critic Agent]
    Critic -- Feedback / Gaps --> Researcher
    Critic -- Verified Data --> Writer[Writer Agent]
    Writer --> Final([Technical Report])
`

## 🚀 Getting Started

### Installation
`ash
git clone https://github.com/TamDoMinh1/Autonomous-Multi-Agent-Researcher.git
cd Autonomous-Multi-Agent-Researcher
pip install -r requirements.txt
`

### Basic Usage
`python
from researcher import ResearchOrchestrator

# Initialize the Orchestrator
orchestrator = ResearchOrchestrator(api_key="your_api_key")

# Execute an autonomous research task
topic = "Impact of Vision Transformers on Real-time Edge Computing"
report = orchestrator.run_study(topic)

print(report)
`

## 🌟 Why this matters?
This framework demonstrates the power of **Agentic Autonomy** in knowledge work. By allowing agents to critique and refine each other's work, we significantly reduce hallucinations and improve the technical depth of AI-generated content.

---
Developed by **Tam Do Minh** - AI Engineer & Researcher