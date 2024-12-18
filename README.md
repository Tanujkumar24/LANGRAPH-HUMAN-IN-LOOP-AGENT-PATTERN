# Human-in-the-Loop System

This project implements a **Human-in-the-Loop (HITL)** system, where human approvals are required for specific actions to ensure correctness. It uses state-of-the-art tools like LangChain, LangGraph, and a custom LLM (`ChatGroq`) to build robust workflows with actionable checkpoints.
### Prerequisites
- Python 3.8+
- Required libraries:
  - `langchain`
  - `langgraph`
  - `langchain-groq`
  - `langchain-community-tools`
  - `IPython`
  - `json`

## Key Features

- **Human-in-the-Loop Workflow**: Integrates human oversight at critical junctures of the decision-making process.
- **State Management**: Utilizes `LangGraph` to manage states and transitions effectively.
- **Custom LLM Integration**: Employs the `ChatGroq` language model (e.g., `Gemma2-9b-It`) for natural language understanding and generation.
- **Tool Nodes**: Implements tools for prebuilt and custom workflows.

## Workflow Overview

Below is a high-level representation of the workflow:

```mermaid
graph TD
    Start[START] --> |Action Initiated| HumanApproval[Human Approval Required?]
    HumanApproval -->|Yes| ManualReview[Manual Review by Human]
    HumanApproval -->|No| AutoProcess[Automated Processing]
    ManualReview --> ActionTaken[Action Completed]
    AutoProcess --> ActionTaken[Action Completed]
    ActionTaken --> End[END]
