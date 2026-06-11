# Awesome NVIDIA NIM [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of resources, tools, projects, and workflows for building with [NVIDIA NIM](https://developer.nvidia.com/nim) — inference microservices for deploying AI models at production scale.

NVIDIA NIM provides optimized, containerized AI model inference via a simple REST API. This list covers everything from getting started to advanced agentic workflows.

**[Submit a PR](https://github.com/DanielDeshmukh/awesome-nvidia-nim/pulls) to add your project!**

---

## Contents

- [Official Resources](#official-resources)
- [Getting Started](#getting-started)
- [Models Available on NIM](#models-available-on-nim)
- [Agentic Workflows & Multi-Agent Systems](#agentic-workflows--multi-agent-systems)
- [RAG Pipelines](#rag-pipelines)
- [CLI Tools & SDKs](#cli-tools--sdks)
- [Integrations](#integrations)
- [Example Projects](#example-projects)
- [Tutorials & Blog Posts](#tutorials--blog-posts)
- [Community & Discussion](#community--discussion)
- [Contributing](#contributing)

---

## Official Resources

- [NVIDIA NIM Overview](https://developer.nvidia.com/nim) — Official landing page and API key signup.
- [NIM API Catalog](https://build.nvidia.com/explore/discover) — Browse all 120+ hosted models (LLMs, VLMs, embeddings, speech, code).
- [NVIDIA Generative AI Examples](https://github.com/NVIDIA/GenerativeAIExamples) — Official RAG and agentic workflow examples.
- [NVIDIA AI Blueprints](https://github.com/NVIDIA-AI-Blueprints) — Production-ready, enterprise reference architectures using NIM.
- [NIM Documentation](https://docs.nvidia.com/nim/) — Full API reference and deployment guides.
- [Metropolis NIM Workflows](https://github.com/NVIDIA/metropolis-nim-workflows) — Visual AI agent workflows using NIM microservices.

## Getting Started

- [NIM Quickstart Guide](https://docs.nvidia.com/nim/large-language-models/latest/getting-started.html) — Get your first API call working in under 5 minutes.
- [NIM Free Credits](https://build.nvidia.com) — 5,000 free credits for all new accounts; no GPU required.
- [OpenAI-Compatible API](https://docs.nvidia.com/nim/large-language-models/latest/openai-api.html) — NIM endpoints are OpenAI-spec compatible; drop-in for any OpenAI SDK client.
- [Deploy Your Own LLM with NIM](https://github.com/NVIDIA-AI-Blueprints/bring-llms-to-nim) — Containerised deployment blueprint for custom models.

## Models Available on NIM

NIM hosts 120+ models across categories. Key ones:

**LLMs**
- `meta/llama-3.3-70b-instruct` — Meta's flagship instruction-tuned model.
- `nvidia/nemotron-4-340b-instruct` — NVIDIA's frontier reasoning model.
- `mistralai/mistral-7b-instruct-v0.3` — Efficient 7B instruction model.
- `microsoft/phi-3-mini-128k-instruct` — Long-context small model.
- `deepseek-ai/deepseek-r1` — Reasoning-focused model.

**Code**
- `qwen/qwen2.5-coder-32b-instruct` — Top-tier code model.
- `ibm/granite-34b-code-instruct` — Enterprise code model.

**Embeddings**
- `nvidia/nv-embedqa-e5-v5` — High-quality retrieval embeddings.
- `baai/bge-m3` — Multilingual embedding model.

**Vision / Multimodal**
- `microsoft/phi-3-vision-128k-instruct` — Vision + language understanding.
- `nvidia/neva-22b` — NVIDIA's VLM.

> Full catalog: [build.nvidia.com/explore/discover](https://build.nvidia.com/explore/discover)

## Agentic Workflows & Multi-Agent Systems

- [autobots](https://github.com/DanielDeshmukh/autobots) ⭐ — PyPI-published CLI for spinning up NVIDIA NIM-powered multi-agent swarms. Supports 120-model live catalog discovery, Tier 1/Tier 2 skill injection, and 465+ tests. `pip install autobot-swarm`
- [NVIDIA Agent Toolkit](https://github.com/NVIDIA/nvidia-agent-toolkit) — Official toolkit for building agent-to-agent (A2A) workflows with NIM.
- [LangGraph + NIM Agents](https://github.com/NVIDIA/GenerativeAIExamples/tree/main/AgentFrameworks) — LangGraph-based multi-agent examples with NIM backends.
- [CrewAI + NIM](https://docs.crewai.com/concepts/llms#nvidia) — Use NIM as LLM backend inside CrewAI agent crews.

## RAG Pipelines

- [RAG with NIM + LangChain](https://github.com/NVIDIA/GenerativeAIExamples/tree/main/RAG) — Production RAG using NIM embeddings + LLM inference.
- [NIM + Qdrant RAG](https://qdrant.tech/documentation/integrations/nvidia-nim/) — Qdrant vector DB integrated with NIM for semantic search.
- [NIM + pgvector](https://github.com/NVIDIA/GenerativeAIExamples/tree/main/RAG/notebooks/langchain) — PostgreSQL pgvector + NIM embeddings pipeline.
- [Knowledge Graph RAG](https://github.com/NVIDIA/GenerativeAIExamples#knowledge-graph-rag) — Graph-augmented retrieval with NIM.

## CLI Tools & SDKs

- [autobot-swarm](https://pypi.org/project/autobot-swarm/) — CLI tool for NIM multi-agent orchestration. Live model discovery, skill injection, swarm configuration. `pip install autobot-swarm`
- [openai Python SDK](https://github.com/openai/openai-python) — Works out-of-the-box with NIM (set `base_url="https://integrate.api.nvidia.com/v1"`).
- [NVIDIA Python SDK (nim)](https://pypi.org/project/nvidia-nim/) — Official Python bindings for NIM microservices.

## Integrations

**Frameworks**
- [LangChain NIM Integration](https://python.langchain.com/docs/integrations/chat/nvidia_ai_endpoints/) — `ChatNVIDIA` class; drop-in for any LangChain chain or agent.
- [LlamaIndex NIM](https://docs.llamaindex.ai/en/stable/examples/llm/nvidia/) — Use NIM as LLM or embedding provider in LlamaIndex pipelines.
- [LangGraph + NIM](https://python.langchain.com/docs/integrations/chat/nvidia_ai_endpoints/) — Build stateful agentic graphs powered by NIM backends.
- [Haystack NIM](https://haystack.deepset.ai/integrations/nvidia) — NVIDIA NIM components for Haystack pipelines.
- [DSPy + NIM](https://dspy.ai) — Use NIM as the LM backend for DSPy programs.

**Vector Stores**
- [Qdrant](https://qdrant.tech/documentation/integrations/nvidia-nim/) — Native NIM embedding integration.
- [Milvus](https://milvus.io/docs/integrate_with_nvidia.md) — NVIDIA NIM + Milvus for large-scale vector search.
- [Weaviate](https://weaviate.io/developers/weaviate/model-providers/nvidia) — NIM embedding and generative modules.

**Infrastructure**
- [NIM on Docker](https://docs.nvidia.com/nim/large-language-models/latest/getting-started.html#deploy-nim) — Self-hosted NIM containers with Docker.
- [NIM on Kubernetes](https://docs.nvidia.com/nim/large-language-models/latest/k8s-operator.html) — Helm charts and K8s operator for NIM deployments.
- [NIM on AWS](https://aws.amazon.com/marketplace/seller-profile?id=nvidia) — NVIDIA NIM AMIs and marketplace listings.

## Example Projects

- [autobots](https://github.com/DanielDeshmukh/autobots) — Multi-agent CLI swarm using NIM. 120-model live catalog. PyPI v0.1.9.
- [AETHER](https://github.com/DanielDeshmukh/aether) — Autonomous pentest platform built on LangGraph + NIM + Playwright.
- [PDF-to-Podcast](https://github.com/NVIDIA-AI-Blueprints/nimttspdf-to-podcast) — Convert PDFs to audio using NIM TTS microservices (210+ stars).
- [H2O Flood Intelligence](https://github.com/h2oai/flood-intelligence-nim) — Real-time flood risk AI with NIM + Nemotron 49B.
- [ChatRAG](https://github.com/mhassaansultan/ChatRAG-NIM) — Gradio-based coding assistant with NIM inference + GitHub context.

## Tutorials & Blog Posts

- [Getting Started with NVIDIA NIM APIs](https://developer.nvidia.com/blog/getting-started-with-nvidia-nim/) — Official NVIDIA walkthrough.
- [Building Agentic AI with NIM and LangGraph](https://developer.nvidia.com/blog/build-ai-agents-with-nvidia-nim-and-langchain/) — End-to-end agent tutorial.
- [RAG in 5 Minutes with NIM](https://developer.nvidia.com/blog/rag-101-retrieval-augmented-generation-with-llms/) — Fast RAG setup guide.
- [NIM vs Ollama: Deploying LLMs Locally](https://developer.nvidia.com/blog/nim-vs-ollama/) — Comparison for local inference.
- [NVIDIA NIM: The Inference Layer for Agentic AI](https://blog.langchain.dev/nvidia-nim-and-langchain/) — LangChain blog on the NIM + LangChain integration.

## Community & Discussion

- [NVIDIA Developer Forums — NIM](https://forums.developer.nvidia.com/c/ai-data-science/nim/535) — Official support and discussion.
- [NVIDIA Discord](https://discord.gg/nvidia) — Community chat with a dedicated AI/NIM channel.
- [r/NVIDIA](https://www.reddit.com/r/nvidia/) — Reddit community.
- [#nvidia-nim on Twitter/X](https://twitter.com/search?q=%23nvidiaNIM) — Community posts and announcements.

---

## Contributing

Contributions welcome! Read the [contribution guidelines](CONTRIBUTING.md) first.

To add a resource:
1. Fork this repo.
2. Add your link in the relevant section — name, URL, and a one-sentence description.
3. Open a pull request.

**Quality bar:** Must be publicly accessible, actively maintained (last commit < 1 year), and directly relevant to NVIDIA NIM. No duplicates, no self-promotion without a working project.

---

*Maintained by [Daniel Deshmukh](https://github.com/DanielDeshmukh) · Mumbai, India*

*If this list helped you, please ⭐ star it — it helps other developers find it.*
