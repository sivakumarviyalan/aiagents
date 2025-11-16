# [Python Quickstart for ADK](https://google.github.io/adk-docs/get-started/python/)

This guide shows you how to get up and running with Agent Development Kit
(ADK) for Python. Before you start, make sure you have the following installed:

*   Python 3.9 or later
*   `pip` for installing packages

## Installation

Create and activate a Python virtual environment

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

Run the `adk create` command to start a new agent project.

```shell
adk create dayXY
```

### Explore the agent project

The created agent project has the following structure, with the `agent.py`
file containing the main control code for the agent.

```none
dayXY/
    agent.py      # main agent code
    .env          # API keys or project IDs
    __init__.py
```

## Update your agent project

The `agent.py` file contains a `root_agent` definition which is the only
required element of an ADK agent. You can also define tools for the agent to
use. 

### Set your API key

This project uses the Gemini API, which requires an API key. If you
don't already have Gemini API key, create a key in Google AI Studio on the
[API Keys](https://aistudio.google.com/app/apikey) page.

In a terminal window, write your API key into an `.env` file as an environment variable:

```console title="Update: dayXY/.env"
echo 'GOOGLE_API_KEY="YOUR_API_KEY"' > .env
```

## Run your agent

You can run your ADK agent with an interactive command-line interface using the
`adk run` command or the ADK web user interface provided by the ADK using the
`adk web` command. Both these options allow you to test and interact with your
agent.

### Run with command-line interface

Run your agent using the `adk run` command-line tool.

```console
adk run dayXY
```

### Run with web interface

The ADK framework provides web interface you can use to test and interact with
your agent. You can start the web interface using the following command:

```console
adk web --port 8000
```

!!! note

    Run this command from the **parent directory** that contains your
    `dayXY/` folder. For example, if your agent is inside `agents/dayXY/`,
    run `adk web` from the `agents/` directory.

This command starts a web server with a chat interface for your agent. You can
access the web interface at (http://localhost:8000). Select the agent at the
upper left corner and type a request.
