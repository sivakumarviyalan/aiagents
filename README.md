# [Python Quickstart for ADK](https://google.github.io/adk-docs/get-started/python/)

This guide shows you how to get up and running with Agent Development Kit
(ADK) for Python. Before you start, make sure you have the following installed:

*   Python 3.9 or later
*   `pip` for installing packages

## Installation

Create a Python virtual environment:

```shell
python -m venv .venv
```

Activate the Python virtual environment in Linux:

```bash
source .venv/bin/activate
```

Install ADK by running the following command:

```shell
pip install google-adk
```

## Create an agent project

### Set your API key

This project uses the Gemini API, which requires an API key. If you
don't already have Gemini API key, create a key in Google AI Studio on the
[API Keys](https://aistudio.google.com/apikey) page.

Run the `adk create` command to start a new agent project.

```shell
adk create my_agent
```

### Explore the agent project

The created agent project has the following structure, with the `agent.py`
file containing the main control code for the agent.

```none
my_agent/
    agent.py      # main agent code
    .env          # API keys or project IDs
    __init__.py
```

## Update your agent project

The `agent.py` file contains a `root_agent` definition which is the only
required element of an ADK agent. You can also define tools for the agent to
use. 

## Run your agent

You can run your ADK agent with an interactive command-line interface using the
`adk run` command or the ADK web user interface provided by the ADK using the
`adk web` command. Both these options allow you to test and interact with your
agent.

### Run with command-line interface

Run your agent using the `adk run` command-line tool.

```console
adk run my_agent
```

### Run with web interface

The ADK framework provides web interface you can use to test and interact with
your agent. You can start the web interface using the following command:

```console
adk web --port 8000
```

### Note:

    Run this command from the **parent directory** that contains your
    `my_agent/` folder. For example, if your agent is inside `aiagents/my_agent/`,
    run `adk web` from the `aiagents/` directory.

This command starts a web server with a chat interface for your agent. You can
access the web interface at (http://localhost:8000). Select the agent at the
upper left corner and type a request.
