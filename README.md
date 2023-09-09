# react-agent-amazon-exhibit99.1
Analyzing Amazon's recent disclosures and attitudes towards LLMs with LlamaIndex's ReAct Agent and Cybersyn data from Snowflake Marketplace

## Application Setup

```
conda create --name py38_env
conda activate py38_env
pip install -r requirements.txt
```

Add `.env` file at the project root and replace placeholder with your OpenAI API key:
```
OPENAI_API_KEY=<YOUR-API-KEY>
```

Add `secrets.toml` to `.streamlit` directory at project root, replace placeholders with your Snowflake connection details:
```
# .streamlit/secrets.toml

[connections.snowpark]
account = "<ORG>-<ACCOUNT>"
user = "<USERNAME>"
password = "<PASSWORD>"
role = "ACCOUNTADMIN"
warehouse = "<WAREHOUSE-NAME>"
database = "CYBERSYN_LLM_TRAINING_ESSENTIALS"
schema = "CYBERSYN"
client_session_keep_alive = true
```

Run the app by kicking off this command:
```
streamlit run react-amazon.py
```

