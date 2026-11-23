# Agentic AI developer tools: 2026 catalog

**Snapshot: 23 November 2026.** This is a practical shortlist for working in existing repositories and building your own engineering agents. Each name links to the project or its official docs. **Popularity** is either approximate GitHub stars observed on that date (`k` = thousand) or a linked adoption example for a managed or open tool. Stars measure interest in the linked repository, not active users, downloads, or production deployments. A dated deployment is direct evidence of use; a current project with stars is a popularity signal, not proof of a 2026 production deployment. Counts for collections and adjacent infrastructure are labeled as such.

For end-to-end examples and the controls companies actually deployed, see the [companion engineering workflows report](agentic-engineering-workflows-2026.md).

## Coding agents and harnesses

| Technology | What it does for a developer | Popularity / observed use |
| --- | --- | --- |
| [OpenCode](https://github.com/anomalyco/opencode) | Multi-provider terminal coding agent with custom agents and a server for integrations. | ~229k stars; [Ramp used it in Inspect](https://builders.ramp.com/post/why-we-built-our-background-agent). |
| [Claude Code](https://github.com/anthropics/claude-code) | Edits repositories, runs shell commands and tests, and supports headless execution, hooks, skills and MCP. | ~157k stars; [Doctolib runs it headlessly](https://claude.com/customers/doctolib). |
| [Codex CLI](https://github.com/openai/codex) | Terminal coding agent with sandbox and approval settings, skills, and noninteractive `exec`. | ~136k stars; [OpenAI used it in its 2026 harness case](https://openai.com/index/harness-engineering/). |
| [Gemini CLI](https://github.com/google-gemini/gemini-cli) | Terminal agent with file, shell and MCP tools; supports headless runs and extensions. | ~109k stars. |
| [OpenHands](https://github.com/OpenHands/OpenHands) | Self-hostable software-agent platform; runs engineering tasks in an isolated workspace via UI, CLI or SDK. | ~94k stars (platform repo). |
| [Cline](https://github.com/cline/cline) | Editor agent that can edit, run commands and call MCP tools, with confirmations or configured auto-approval. | ~72k stars. |
| [goose](https://github.com/aaif-goose/goose) | Local extensible agent with MCP tools and reusable recipes; run it via desktop or CLI. | ~57k stars; [Stripe forked it for Minions](https://stripe.dev/blog/minions-stripes-one-shot-end-to-end-coding-agents-part-2). |
| [Aider](https://github.com/Aider-AI/aider) | Terminal pair programmer that uses a repository map to drive multi-file edits and can commit changes to Git. | ~50k stars. |
| [Continue](https://github.com/continuedev/continue) | Configurable IDE and CLI tooling for coding agents and headless repository checks. | ~37k stars (project repo). |
| [GitHub Copilot CLI](https://github.com/github/copilot-cli) | Terminal agent with skills, custom agents and shell-tool approvals. | ~11.5k stars (CLI repo only); [GitHub used Copilot for its runtime port](https://github.blog/ai-and-ml/generative-ai/migrating-the-github-copilot-runtime-to-rust-using-copilot/). |
| [Cursor](https://cursor.com/docs/cloud-agent) | Editor-based coding agent; its Cloud Agents feature can also run tasks asynchronously in remote environments. | [Grab documents Cursor calling Scarlet](https://engineering.grab.com/how-grab-built-scarlet-blog); no Cloud Agents usage figure established. |
| [Devin](https://docs.devin.ai/get-started/devin-intro) | Hosted coding agent with a remote workspace that can run tests and open PRs. | [NASA JPL F Prime merged a Devin-authored fix and regression test](https://github.com/nasa/fprime/pull/6083). |
| [Kiro](https://kiro.dev/docs/) | Spec-driven coding agent that turns requirements and design into tasks, with steering files and hooks. | [Southwest reported 2,700+ developers using Kiro](https://investors.southwest.com/news-events/press-releases/detail/1932/southwest-airlines-partners-with-amazon-web-services-aws-to-accelerate-ai-capabilities-and-technology-modernization), not all on the website refactor. |
| [AWS Transform](https://docs.aws.amazon.com/transform/latest/userguide/) | Managed modernization agents for work such as dependency upgrades and containerization; not an everyday editor agent. | [British Airways](https://aws.amazon.com/blogs/devops/how-british-airways-is-accelerating-the-modernization-of-its-java-services/) used it on Java services; [Kuehne+Nagel](https://aws.amazon.com/blogs/migration-and-modernization/20-times-faster-kuehnenagel-containerizes-enterprise-apps-in-hours-with-aws-transform/) containerized ten in-scope applications. |

## Agent SDKs and orchestration

| Technology | What it does for a developer | Popularity / observed use |
| --- | --- | --- |
| [LangGraph](https://github.com/langchain-ai/langgraph) | Model an agent as a state graph with checkpoints, branching, durable execution and human interrupts. | ~45k stars; [Grab uses interrupts to pause and resume Scarlet](https://engineering.grab.com/how-grab-built-scarlet-blog). |
| [Deep Agents](https://github.com/langchain-ai/deepagents) | Higher-level harness built on LangGraph with planning, file tools and subagents; use it rather than writing the whole loop. | ~32k stars. |
| [Claude Agent SDK](https://github.com/anthropics/claude-agent-sdk-python) | Embed the Claude Code agent loop and built-in tools in a Python or TypeScript application. | ~8.6k stars (Python repo); [Spotify built Honk around the SDK](https://engineering.atspotify.com/2026/6/code-with-claude-coding-is-no-longer-the-constraint). |
| [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) | Build Python tool loops with agent handoffs, guardrails and tracing; [TypeScript SDK](https://github.com/openai/openai-agents-js) also available. | ~31k Python / ~4k TypeScript stars. |
| [CrewAI](https://github.com/crewAIInc/crewAI) | Combine role-based agents in Crews; use Flows to define events, state and branching around them. | ~61k stars. |
| [Google Agent Development Kit](https://github.com/google/adk-python) | Compose tool-using agents with sequential, parallel and loop workflows; test them locally. | ~22k stars (Python repo). |
| [Pydantic AI](https://github.com/pydantic/pydantic-ai) | Python agent SDK with typed dependencies and outputs, tool validation and testing hooks. | ~21k stars. |
| [Mastra](https://github.com/mastra-ai/mastra) | TypeScript framework for agents, typed workflows, memory and evaluations in Node applications. | ~30k stars. |
| [Strands Agents](https://github.com/strands-agents/harness-sdk) | Python SDK for assembling a model-driven agent loop with tools; add graph or multi-agent patterns when needed. | ~9.3k stars (harness SDK repo). |
| [smolagents](https://github.com/huggingface/smolagents) | Lightweight Python agent library; select structured tool calls or a code-writing loop. Isolate execution when enabling the latter. | ~31k stars. |
| [Vercel AI SDK](https://github.com/vercel/ai) | TypeScript primitives for streaming model output, calling tools and building agent loops into web UIs. | ~28k stars (SDK overall). |
| [Temporal](https://github.com/temporalio/temporal) | Durable workflow engine for retrying and resuming explicit activities; put model calls in activities rather than replayed workflow code. | ~25k stars (general workflow engine, not an agent-specific metric). |
| [n8n](https://github.com/n8n-io/n8n) | Visual workflow builder with agent and tool nodes; wire Slack, issue trackers and webhooks around model calls. | ~212k stars (entire automation project). |
| [Agent2Agent (A2A)](https://github.com/a2aproject/A2A) | Protocol for separately hosted agents to advertise capabilities and exchange tasks, status and artifacts. Not a scheduler or a replacement for MCP tool calls. | ~27k stars (protocol repo). |

## MCP: connect agents to concrete tools

| Technology | What it does for a developer | Popularity / observed use |
| --- | --- | --- |
| [MCP reference servers](https://github.com/modelcontextprotocol/servers) | Read server examples for filesystem, Git and other integrations; review permissions before using them on a real repo. | ~92k stars (collection, not one server). |
| [MCP Python SDK](https://github.com/modelcontextprotocol/python-sdk) / [TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk) | Implement MCP clients and servers, define schemas, and expose tools, resources or prompts over supported transports. | ~25k Python / ~14k TypeScript stars. |
| [FastMCP](https://github.com/PrefectHQ/fastmcp) | Turn Python functions into typed MCP tools and compose or proxy servers. | ~29k stars. |
| [GitHub MCP Server](https://github.com/github/github-mcp-server) | Read repository context, issues and PRs or perform scoped writes; enable only the toolsets a task needs. | ~35k stars. |
| [Playwright MCP](https://github.com/microsoft/playwright-mcp) | Give agents structured browser interaction, including accessibility snapshots, to reproduce UI bugs or verify a fix. | ~40k stars. |
| [Context7](https://github.com/upstash/context7) | Fetch library docs and examples into the coding session; specify the dependency version when possible. | ~65k stars. |
| [Sentry MCP / toolkit](https://github.com/getsentry/toolkit) | Pull Sentry issues and event context into a debugging session rather than copying stack traces by hand. | ~1k stars (toolkit repo). |
| [AWS Labs MCP servers](https://github.com/awslabs/mcp) | AWS-specific integrations for docs, service context and infrastructure tasks; start with read-only access. | ~9.9k stars (collection). |
| [Docker MCP Gateway](https://github.com/docker/mcp-gateway) | Configure and run containerized MCP servers behind a common endpoint for local clients. | ~1.6k stars. |

## Skills, repository instructions and CI integrations

| Technology or pattern | What it does for a developer | Popularity / observed use |
| --- | --- | --- |
| [Agent Skills](https://github.com/agentskills/agentskills) | Package a repeatable procedure in `SKILL.md`, with optional scripts, references and assets. Load detailed instructions only when needed. | ~28k stars (spec repo). |
| [AGENTS.md](https://github.com/agentsmd/agents.md) | Keep durable repo instructions close to the code: build/test commands, architectural boundaries, and where to find deeper guidance. | ~26k stars; [OpenAI used a short file as a map](https://openai.com/index/harness-engineering/). |
| [Anthropic Skills](https://github.com/anthropics/skills) | Examples of packaged instructions and supporting scripts; useful templates for writing internal skills. | ~199k stars (examples collection). |
| [OpenAI Skills](https://github.com/openai/skills) | Codex skill catalog; inspect and pin useful examples rather than silently tracking updates. | ~29k stars (catalog). |
| [Claude Code Action](https://github.com/anthropics/claude-code-action) | Run Claude from GitHub Actions for issues or PRs; wire repository events to a headless run with explicit permissions. | ~10k stars. |
| [Codex GitHub Action](https://github.com/openai/codex-action) | Invoke Codex from a GitHub Actions job for scoped tasks such as summarizing a failed check or reviewing a change. | ~1.3k stars. |
| [Repository-local verification skills](https://claude.dev/blog/how-the-claude-code-team-thinks-about-verification/) | Wrap a deterministic check in a small skill: how to boot the app, exercise it, and collect evidence. Keep permissions in the runner, not the skill. | [Anthropic uses `verify` skills](https://claude.dev/blog/how-the-claude-code-team-thinks-about-verification/); [JPL merged a framework navigation skill](https://github.com/nasa/fprime/pull/6312). |

## Sandboxing and remote execution

| Technology | What it does for a developer | Popularity / observed use |
| --- | --- | --- |
| [E2B](https://github.com/e2b-dev/E2B) | API-managed Linux sandboxes with terminal, filesystem and templates for running agent-generated code. | ~15k stars. |
| [Modal Sandboxes](https://modal.com/docs/guide/sandboxes) | Start a managed isolated process from a prepared image or snapshot; use it for per-task coding environments. | [Ramp documents Modal for Inspect](https://builders.ramp.com/post/why-we-built-our-background-agent). |
| [Firecracker](https://github.com/firecracker-microvm/firecracker) | Linux/KVM microVM building block for stronger workload isolation; supply your own workspace, network and credential policy. | ~38k stars (general isolation infrastructure). |
| [gVisor](https://github.com/gvisor/gvisor) | Run containers with `runsc`, which interposes a userspace kernel; evaluate syscall compatibility for builds and tests. | ~20k stars (general isolation infrastructure). |
| [Palana](https://engineering.grab.com/part-2-palana-architecture) | Grab’s documented design: Kubernetes namespaced runs, Cilium default-deny policies, OPA egress checks and Vault-backed proxy credentials. A reference architecture, not a distributable SDK. | Grab’s documented production platform; not confirmed as Scarlet’s runtime. |

## Model routing, browser tools, evaluations and telemetry

| Technology | What it does for a developer | Popularity / observed use |
| --- | --- | --- |
| [LiteLLM](https://github.com/BerriAI/litellm) | Put a common API, routing and budget controls in front of multiple model providers; does not orchestrate tool calls. | ~64k stars; [Delivery Hero uses its proxy](https://claude.com/customers/delivery-hero). |
| [Playwright](https://github.com/microsoft/playwright) | Turn an agent’s browser reproduction into a deterministic, repeatable UI check with assertions and traces. | ~101k stars (general test tool, not MCP adoption). |
| [Stagehand](https://github.com/browserbase/stagehand) | Combine browser automation code with natural-language actions and structured extraction when selectors alone are brittle. | ~26k stars. |
| [Browser Use](https://github.com/browser-use/browser-use) | Python browser-agent library for navigating pages and doing multi-step UI tasks; keep its browser credentials scoped. | ~122k stars. |
| [SWE-bench](https://github.com/SWE-bench/SWE-bench) | Benchmark patch generation against real issue/repo tasks and executable tests; supplement with private repo-specific replays. | ~6.2k stars (benchmark tooling repo). |
| [Promptfoo](https://github.com/promptfoo/promptfoo) | Compare model/prompt configurations with fixtures and assertions in CI; useful for regression tests around model outputs. | ~28k stars. |
| [Langfuse](https://github.com/langfuse/langfuse) | Trace model and tool calls; turn selected traces into datasets and run evaluations on them. | ~38k stars. |
| [Arize Phoenix](https://github.com/Arize-ai/phoenix) | Inspect model/tool traces, latency and errors; run evaluations against curated datasets. | ~12k stars. |
| [OpenTelemetry GenAI conventions](https://opentelemetry.io/docs/specs/semconv/gen-ai/) | Standardize model telemetry across vendors; check each convention’s stability before relying on it. Avoid exporting secrets or code by default. | [~4.4k stars for the overall OTel specification](https://github.com/open-telemetry/opentelemetry-specification), not the GenAI subset. |
| [DSPy](https://github.com/stanfordnlp/dspy) | Define model components with signatures and optimize them against a dataset and metric; useful when changing a prompt by hand stops scaling. | ~39k stars. |

**A practical starting stack:** Pick one harness, put build/test commands in `AGENTS.md`, package one repeatable task as a skill, and run it with scoped credentials in an isolated workspace. Prefer a reviewed CLI command when it already does the job; add MCP when several agents need the same typed integration. Add a workflow engine when you need durable retries or approval pauses, and evaluate changes against private replay fixtures and deterministic tests before expanding autonomy.
