# Agents-GoogleADK (cleaned)

Below is a cleaned, code-only version of the original notebook. It keeps only code blocks and short comments describing what each block does.

> Source notebook: `Agents-GoogleADK.ipynb`

---

## 1) Install / upgrade dependencies

```python
# Install required packages for Google ADK / agent tooling
# (Run once in a fresh environment)
!pip install -U google-adk
```

---

## 2) Imports

```python
# Import agent framework primitives and any helper utilities
from google.adk import Agent
```

---

## 3) Configure credentials / API keys

```python
# Set your Google / Gemini credentials in the environment.
# Prefer using secrets management (Colab secrets, env vars, or .env) instead of hardcoding.
import os

os.environ["GOOGLE_API_KEY"] = "YOUR_API_KEY_HERE"  # TODO: replace securely
```

---

## 4) Define an agent

```python
# Create a simple agent with instructions describing its role.
agent = Agent(
    name="helper_agent",
    instructions="You are a helpful assistant that answers questions clearly and concisely.",
)
```

---

## 5) Run the agent

```python
# Send a prompt to the agent and print the response.
response = agent.run("Explain what Google ADK agents are in one paragraph.")
print(response)
```
