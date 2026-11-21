<h1 align="center">Hi 👋, I'm Franklin Sandoval</h1>
<h3 align="center">DevOps &amp; AI Engineer | Software Engineer from Costa Rica 🇨🇷</h3>
<p align="center"><i>I build backend systems and LLM-powered apps, and I ship them on containers and the cloud.</i></p>

<p align="center">
  <a href="https://www.linkedin.com/in/franklin-sandoval"><img src="https://img.shields.io/badge/LinkedIn-Franklin%20Sandoval-0A66C2?logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://www.upwork.com/freelancers/~0122ff330fa98c4c92"><img src="https://img.shields.io/badge/Upwork-Hire%20me-6FDA44?logo=upwork&logoColor=white" alt="Upwork" /></a>
  <a href="mailto:franklin.sandoval42@gmail.com"><img src="https://img.shields.io/badge/Email-franklin.sandoval42%40gmail.com-EA4335?logo=gmail&logoColor=white" alt="Email" /></a>
  <img src="https://komarev.com/ghpvc/?username=franklin34&label=Profile%20views&color=0e75b6&style=flat" alt="Profile views" />
</p>

---

## 🤖 What I'm building

- 🧠 **LLM applications:** chatbots with streaming responses, conversation memory, and provider-agnostic design (Gemini, Claude, OpenAI-compatible APIs)
- 🤖 **Agent systems with real guard rails:** tool-using agents (Google ADK, MCP) where safety is enforced in code, not in prompts
- ☸️ **Cloud-native infrastructure and DevOps:** containers, CI/CD and infrastructure as code
- 🌱 Currently deepening my skills in **Kubernetes, Terraform, Docker and AWS**
- 👯 Open to collaborating on **AI, backend and DevOps projects**
- 💬 Ask me about **LLM integration, DevOps, Python, Java**

## ⭐ Featured projects

### [AI Chatbot](https://github.com/franklin34/AI_Chatbot): production-minded LLM chat app

A streaming chatbot with a **FastAPI** backend and a provider-agnostic core. One environment variable switches between Google Gemini, Anthropic Claude, or any OpenAI-compatible API (OpenAI, Groq, OpenRouter, local Ollama).

- Token-by-token streaming over Server-Sent Events, rendered as sanitized Markdown
- Multi-turn memory with a sliding context window to keep cost and latency bounded
- Retries with exponential backoff on rate limits and overload, with no duplicated output
- Rate limiting, input validation, typed config, structured logging
- Tests that run without an API key, plus Docker and CI (GitHub Actions)

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/CI-GitHub%20Actions-2088FF?logo=githubactions&logoColor=white)

### [Pipeline Doctor](https://github.com/Franklin34/pipeline-doctor-agent): AI agent that investigates failed CI pipelines, safely

When a Jenkins build fails, this system finds the likely root cause in the code history, writes the Jira ticket, and, when it is safe, opens a **draft** pull request with a fix that was tested in an isolated sandbox. The design rule: **the model proposes, code decides, humans merge.**

- **Go** webhook ingress (HMAC-verified, de-duplicated) feeding a queue (Redis Streams or **Google Pub/Sub**), consumed by a **Python worker on Google ADK**, with tools served over **MCP** (Go and Python servers)
- Safety enforced in code: per-agent tool allowlists, a policy gate, prompt-injection screening, and a model that has **no write tools**; the agent never merges or pushes to the default branch
- Fixes proposed as edits and tested in a **Docker sandbox** (no network, read-only filesystem, non-root, resource limits) before any draft PR
- Hybrid retrieval over runbooks and past incidents (**Postgres + pgvector**); **OpenTelemetry**, Prometheus and Grafana for traces, metrics and alerts
- Golden-dataset **evals with mutation tests** that prove the safety checks can actually fail; 700+ tests; **Terraform** for Google Cloud (validated, not yet applied)
- Try it with no API key: `make demo` runs the real pipeline end to end with a scripted model

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?logo=go&logoColor=white)
![Google ADK](https://img.shields.io/badge/Google%20ADK-4285F4?logo=google&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-000000?logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?logo=terraform&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-425CC7?logo=opentelemetry&logoColor=white)
![Google Cloud](https://img.shields.io/badge/Google%20Cloud-4285F4?logo=googlecloud&logoColor=white)

## 🛠️ Tech stack

**AI &amp; Backend**

![Python](https://skillicons.dev/icons?i=python,go,fastapi,java,spring,nodejs,ts,js&theme=dark)
&nbsp;LLM APIs: Gemini · Claude · OpenAI-compatible (SSE streaming, prompt/context management) · Agents: Google ADK · MCP

**DevOps &amp; Cloud**

![DevOps](https://skillicons.dev/icons?i=docker,kubernetes,terraform,aws,gcp,githubactions,jenkins,linux,bash,nginx,grafana,prometheus&theme=dark)

**Data &amp; Messaging**

![Data](https://skillicons.dev/icons?i=postgres,mysql,mongodb,redis,kafka&theme=dark)

**Frontend &amp; Tools**

![Tools](https://skillicons.dev/icons?i=angular,html,css,git,postman&theme=dark)

## 📊 GitHub stats

<p>
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=franklin34&show_icons=true&locale=en&hide_border=true" alt="GitHub stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs?username=franklin34&layout=compact&locale=en&hide_border=true" alt="Top languages" />
</p>

## 📫 Let's connect

Looking for an engineer who can take an AI or backend idea from concept to a working, deployed system? Hire me on [Upwork](https://www.upwork.com/freelancers/~0122ff330fa98c4c92), email **franklin.sandoval42@gmail.com**, or find me on [LinkedIn](https://www.linkedin.com/in/franklin-sandoval).
