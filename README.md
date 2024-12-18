
# LANGRAPH-HUMAN-IN-LOOP-AGENT-PATTERN

This repository demonstrates the implementation of a human-in-the-loop (HITL) agent pattern using LangGraph. 
The approach integrates human input into automated processes, enhancing decision-making and ensuring accuracy in language model outputs.

## Overview

Human-in-the-loop systems combine automated processes with human judgment, allowing for interventions at critical stages. 
In language model applications, this integration ensures outputs are accurate and contextually appropriate. 
This project showcases how to implement such a system using LangGraph.

## Features

- **LangGraph Agent Integration**: Utilizes LangGraph to manage the workflow of language models.
- **Tool Integration**: Incorporates external tools to enhance the agent's capabilities.
- **Human Feedback Loop**: Allows human intervention to review and modify outputs, ensuring accuracy.

## Getting Started

### Prerequisites

Ensure you have the following installed:

- Python 3.8 or higher
- Necessary Python packages (listed in `requirements.txt`)

### Installation

1. **Clone the repository**:

```bash
git clone https://github.com/Tanujkumar24/LANGRAPH-HUMAN-IN-LOOP-AGENT-PATTERN.git
```

2. **Navigate to the project directory**:

```bash
cd LANGRAPH-HUMAN-IN-LOOP-AGENT-PATTERN
```

3. **Install the required packages**:

```bash
pip install -r requirements.txt
```
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


### Usage

The main implementation is in the Jupyter Notebook `human_in_loop.ipynb`.
To run it:

1. **Start Jupyter Notebook**:

```bash
jupyter notebook
```

2. **Open `human_in_loop.ipynb`**: Navigate through the cells, executing them sequentially to understand and run the human-in-the-loop agent pattern.

## Implementation Details

### LangGraph Agent

The agent is set up using LangGraph's `ChatBedrock` model, configured with specific parameters to manage the language model's behavior.

### Tool Integration

The agent incorporates external tools, such as `TavilySearchResults`, to enhance its capabilities.

### Human Feedback Loop

A function named `should_continue` determines whether the process should proceed automatically or await human input, enabling human intervention when necessary.

## Contributing

Contributions are welcome. Please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License.

## Acknowledgments

Special thanks to the developers of LangGraph and the contributors to the human-in-the-loop concept.

For more information on human-in-the-loop implementations with LangGraph, refer to the [LangGraph Human-in-the-loop Documentation](https://langchain-ai.github.io/langgraph/concepts/human_in_the_loop/).
