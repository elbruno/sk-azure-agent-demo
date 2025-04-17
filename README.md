<!-- filepath: d:\elbruno\sk-azure-agent-demo\README.md -->
# Semantic Kernel + Azure AI Agent demo

In this demo, we will show how to use the Semantic Kernel process framework to orchestrate
multiple Azure AI Agent Service agents.

## Prerequisites
You'll need an Azure AI Foundry project with the following agents. You can find the code to create these agents in the `agents` folder.

- [Researcher agent](./agents/researcher_agent.py)
- [Writer agent](./agents/writer_agent.py)
- [Editor agent](./agents/editor_agent.py)
- [Publisher agent](./agents/publisher_agent.py)

### Python Environment Setup
To work with the Python agents, you'll need to set up a virtual environment and install the required dependencies:

1. Create a virtual environment:
```bash
python -m venv venv
```

2. Activate the virtual environment:
```bash
# On Windows
venv\Scripts\Activate.ps1
# On Linux/Mac
source venv/bin/activate
```

3. Install the dependencies:
```bash
pip install -r requirements.txt
```

The `requirements.txt` file includes the following dependencies:
- python-dotenv - For loading environment variables
- azure-ai-projects - For working with AI Project Client
- azure-identity - For Azure authentication
- pyyaml - For working with YAML files

## Running the demo
To run the demo, first copy the `sample.env` file to `.env` and fill in the required values.

Then update the `./agents/tools/send_email.yaml` file with the endpoint of your send email API.

Then, run the following command:

```bash
dotnet build
dotnet run
```