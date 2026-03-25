<!-- BlackRoad SEO Enhanced -->

# ollama models

> Part of **[BlackRoad OS](https://blackroad.io)** — Sovereign Computing for Everyone

[![BlackRoad OS](https://img.shields.io/badge/BlackRoad-OS-ff1d6c?style=for-the-badge)](https://blackroad.io)
[![BlackRoad-AI](https://img.shields.io/badge/Org-BlackRoad-AI-2979ff?style=for-the-badge)](https://github.com/BlackRoad-AI)

**ollama models** is part of the **BlackRoad OS** ecosystem — a sovereign, distributed operating system built on edge computing, local AI, and mesh networking by **BlackRoad OS, Inc.**

### BlackRoad Ecosystem
| Org | Focus |
|---|---|
| [BlackRoad OS](https://github.com/BlackRoad-OS) | Core platform |
| [BlackRoad OS, Inc.](https://github.com/BlackRoad-OS-Inc) | Corporate |
| [BlackRoad AI](https://github.com/BlackRoad-AI) | AI/ML |
| [BlackRoad Hardware](https://github.com/BlackRoad-Hardware) | Edge hardware |
| [BlackRoad Security](https://github.com/BlackRoad-Security) | Cybersecurity |
| [BlackRoad Quantum](https://github.com/BlackRoad-Quantum) | Quantum computing |
| [BlackRoad Agents](https://github.com/BlackRoad-Agents) | AI agents |
| [BlackRoad Network](https://github.com/BlackRoad-Network) | Mesh networking |

**Website**: [blackroad.io](https://blackroad.io) | **Chat**: [chat.blackroad.io](https://chat.blackroad.io) | **Search**: [search.blackroad.io](https://search.blackroad.io)

---


**Local LLM inference with custom model configurations**

## Quick Start

```bash
# Install Ollama
curl -fsSL https://ollama.com/install.sh | sh

# Pull BlackRoad models
./scripts/pull-all.sh

# Run a model
ollama run blackroad-coder
```

## Custom Models

### BlackRoad Coder (Code Generation)
```bash
ollama create blackroad-coder -f models/blackroad-coder.Modelfile
```

### BlackRoad Analyst (Data Analysis)
```bash
ollama create blackroad-analyst -f models/blackroad-analyst.Modelfile
```

### BlackRoad Agent (Task Execution)
```bash
ollama create blackroad-agent -f models/blackroad-agent.Modelfile
```

## Model Configurations

| Model | Base | Size | Quantization | Purpose |
|-------|------|------|--------------|---------|
| blackroad-coder | codellama:34b | 19GB | Q4_K_M | Code gen |
| blackroad-analyst | mistral:7b | 4.1GB | Q4_0 | Analysis |
| blackroad-agent | llama3:8b | 4.7GB | Q4_0 | Tasks |
| blackroad-phi | phi3:mini | 2.3GB | Q4_0 | Fast inference |

## API Usage

```python
import ollama

response = ollama.chat(model='blackroad-coder', messages=[
    {'role': 'user', 'content': 'Write a Python function for Fibonacci'}
])
print(response['message']['content'])
```

## Fleet Deployment

Deploy across all BlackRoad devices:

```bash
for host in cecilia lucidia alice aria; do
  ssh $host 'ollama pull mistral:7b'
done
```

---

*BlackRoad OS - Local AI Power*
