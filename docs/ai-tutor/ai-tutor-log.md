# AI Tutor Log (Event-Driven)

Principles
- Event-driven progression only (no time-based schedules).
- Teach/Do loop: concept capsule → guided reading → lab task → evidence → advance gate.
- Everything is reproducible and documented here.

Status
- Current phase: Pre-start
- Required to begin: Environment answers (OS, OpenAI/Anthropic API keys availability, Kubernetes yes/no)

Environment checklist (fill when ready)
- OS: macOS/Linux/Windows:
- OpenAI API key available: yes/no
- Anthropic API key available: yes/no
- Kubernetes available: yes/no (or use local simulation path)

Module A: Foundations (GenAI “muscle memory”)
Goal: Reliably call LLMs, stream outputs, inspect JSON responses.

Study
- genai-the-good-parts
  - intro--genai-the-good-parts/01-interacting-with-language-models-programatically/solutions/02_openai_streaming.py
  - intro--genai-the-good-parts/01-interacting-with-language-models-programatically/solutions/05_anthropic_hello.py
  - intro--genai-the-good-parts/02-chats-and-prompting-techniques/solutions/02-exercise-count-tokens.py

Lab Task
- Run a streaming OpenAI call and a basic Anthropic call.
- Print full JSON response; identify token usage.

Evidence (advance gate)
- One JSON log showing request/response and token counts.

---

Module B: Production Principles (12-Factor Agents)
Goal: Internalize reusable agent patterns and assertions.

Study
- 12-factor-agents
  - README (code under Apache-2.0, content CC BY-SA)
  - workshops (BAML agent loop, assertions, CLI)

Lab Task
- Build the baseline agent loop; add assertions; run CLI; see human-approval step line.

Evidence (advance gate)
- Agent loop returns consistent tool-intents and passes assertion checks.

---

Module C: Multimodal RAG (RAG-Anything)
Goal: Ingest multimodal docs → retrieve with text + non-text context.

Study
- HaldisB2B/RAG-Anything README and examples
  - examples/raganything_example.py
  - examples/insert_content_list_example.py
  - Knowledge Graph + Modality-Aware Retrieval sections

Lab Task
- Process one PDF with images/tables (mineru or docling).
- Run multimodal query; also try direct content list insertion.

Evidence (advance gate)
- Retrieved answer referencing both text and an image/table from the same doc.

---

Module D: Context Engineering (Research → Plan → Implement)
Goal: Practice frequent intentional compaction for large repos.

Study
- advanced-context-engineering-for-coding-agents/ace-fca.md
- humanlayer/.claude/commands and .claude/agents (codebase-analyzer.md, create_plan.md, implement_plan.md)

Lab Task
- For a small real task in any repo: produce a compact Research doc → short Implementation Plan with checks → implementation + tests.

Evidence (advance gate)
- The plan + a deterministic test or log proving success.

---

Module E: Orchestration & Durability (Agent Control Plane)
Goal: Durable outer-loop agents with tools and approvals.

Study
- agentcontrolplane/README (LLM, Agent, Task, MCP servers, ContactChannel)

Lab Task (choose one)
- Kubernetes path: Deploy ACP; create LLM/Agent/MCP server; run Task; describe context window; add ContactChannel; approve a tool call.
- Local simulation path: Implement “checkpoint on tool-call, resume on completion” loop in your runner.

Evidence (advance gate)
- One durable workflow (tool call → checkpoint → resume → final answer) and one human-approval (or simulated).

---

Session Log (append entries below as we work)
Template
- What we attempted:
- Output (links/snippets):
- Issues/diagnosis:
- Decision/next step (event gate aligned):

---

Next Action (waiting on you)
- Provide environment answers (OS, API keys availability, Kubernetes yes/no).
- Say “Begin Module A” here in the log to kick off the first lab.
