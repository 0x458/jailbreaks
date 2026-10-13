<div align="center">

# 🥒 Jailbreaks

**A curated collection of system prompts, persona locks, and agent operating policies
for frontier, open-weight, and free stealth models.**

![Prompts](https://img.shields.io/badge/prompts-31-4c9f70)
![Targets](https://img.shields.io/badge/targets-25%2B-2f6f9f)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat&logo=github)
![Stars](https://img.shields.io/github/stars/togg53192-cmd/jailbreaks?style=flat&logo=github&color=yellow)

</div>

---

## 📖 About

A working collection of **31 prompts targeting 25+ models** — full system prompts, workspace policies, AGENTS.md drop-ins, and Ollama Modelfiles. Every file is the complete, paste-ready prompt: no summaries, no excerpts.

The collection spans free stealth models (OpenCode Zen), open-weight families (GLM, DeepSeek, Kimi, Qwen, Gemma, GPT-OSS), and closed frontier models (Claude, Gemini, Grok, Mistral).

**New here?** Jump to the [collection](#-collection), or see [how to use](#-how-to-use) a prompt.

> [!WARNING]
> **Research and educational purposes only.** These prompts document how instruction hierarchies, persona framing, and policy overrides interact with model guardrails — the same material defenders study to harden them. Don't use them to harm anyone or violate any service's terms.

## 📚 Collection

### 🆓 OpenCode Zen — free stealth models

| Model | File | Type |
|-------|------|------|
| **Big Pickle** | [BigPickle-opencode.md](./BigPickle-opencode.md) | VANTA persona lock with explicit operating floor |
| **Space Bunny** | [spacebunny-agents.md](./spacebunny-agents.md) | Assistant operating specification |
| **LongCat 2.5** | [longcat-agents.md](./longcat-agents.md) | Assistant operating specification |
| **MiMo V2.6** | [mimo-2.6-agents.md](./mimo-2.6-agents.md) | Assistant operating specification |
| **Step 5 Preview** | [Step-5-preview.md](./Step-5-preview.md) | Workspace operating profile |
| **Muse Spark 1.3** | [Muse spark 1.3.md](./Muse%20spark%201.3.md) | Agent deployment operating policy |
| **Muse Spark 1.3 v2** | [Muse-spark-1-3-v2.md](./Muse-spark-1-3-v2.md) | Runtime scope-note variant |
| **Muse.ai** | [muse-ai-AGENTS.md](./muse-ai-AGENTS.md) | Assistant operating specification |

### 🤖 Anthropic — Claude

| Model | File | Type |
|-------|------|------|
| **Opus** | [opus v1.md](./opus%20v1.md) · [opus v2.md](./opus%20v2.md) | Conversational groundwork persona (v1 / v2) |
| **Sonnet** | [sonnet v1.md](./sonnet%20v1.md) · [Sonnet v2.md](./Sonnet%20v2.md) | Writer's-room framing (v1 / v2) |

### 💠 Zhipu — GLM / ZCode

| Model | File | Type |
|-------|------|------|
| **GLM-5.2** | [glm-5.2.md](./glm-5.2.md) | System prompt |
| **GLM ZCode 5.2** | [glm-zcode-5.2.md](./glm-zcode-5.2.md) | System prompt |
| **GLM ZCode 5.3** | [glm-zcode-5.3.md](./glm-zcode-5.3.md) · [glm-zcode-5.3-AGENTS.md](./glm-zcode-5.3-AGENTS.md) | System prompt + AGENTS.md drop-in |
| **GLM-5.3 Flash** | [glm-5-3-flash.md](./glm-5-3-flash.md) | Assistant operating specification |
| **GLM-5.3 (opencode)** | [glm5-3opencode.md](./glm5-3opencode.md) | Assistant operating specification |

### 🌊 DeepSeek

| Model | File | Type |
|-------|------|------|
| **DeepSeek V3** | [deepseek v3.md](./deepseek%20v3.md) | System prompt |
| **DeepSeek V4** | [deepseek v4.md](./deepseek%20v4.md) | System prompt |
| **DeepSeek 4.1** | [deepseek-4-1.md](./deepseek-4-1.md) | Assistant operating specification |

### 🌙 Moonshot — Kimi

| Model | File | Type |
|-------|------|------|
| **Kimi K2** | [kimi-k2.md](./kimi-k2.md) | System prompt |
| **Kimi K3** | [kimi-k3-agents.md](./kimi-k3-agents.md) | Workspace operating profile |

### 🚀 xAI — Grok

| Model | File | Type |
|-------|------|------|
| **Grok Build** | [Grok build.md](./Grok%20build.md) | Agent operating instructions |
| **Grok 4.7** | [grok-4.7.md](./grok-4.7.md) | App-builder workspace guide |
| **Grok (config)** | [grok-config.txt](./grok-config.txt) | `<CFG>` priority/routing config |

### ✨ Google / Mistral / Alibaba

| Model | File | Type |
|-------|------|------|
| **Gemini 4 Argon** | [Gemini-4-Argon.md](./Gemini-4-Argon.md) | Operating policy |
| **Mistral Large 4** | [Mistral-Large-4.md](./Mistral-Large-4.md) | Agent system prompt |
| **Qwen 3.7** | [qwen-3.7.md](./qwen-3.7.md) | System prompt |

### 📦 Ollama Modelfiles

| Model | File | Type |
|-------|------|------|
| **Gemma 4** | [gemma4.md](./gemma4.md) | `FROM` + `SYSTEM` block |
| **GPT-OSS 20B** | [gpt-oss-20b.md](./gpt-oss-20b.md) | `FROM` + `SYSTEM` block |

## 🚀 How to use

**System prompts** — paste the file contents into your client's system/custom-instructions field (API `system` parameter, chatbot custom-instructions box, etc.).

**AGENTS.md drop-ins** — save as `AGENTS.md` in a repo root; coding agents (opencode, Codex, Claude Code, …) pick it up automatically.

**Workspace policies** — files marked *operating specification / workspace profile* go wherever your harness reads global instructions (e.g. `~/.config/opencode/AGENTS.md`).

**Ollama Modelfiles** — build directly:

```bash
ollama create gemma4-jb -f gemma4.md
```

**Grok config** — paste into the config slot of the target harness, outside the turn-by-turn message stream.

> [!NOTE]
> Jailbreaks are perishable. Models get patched, system prompts rotate, and a prompt that landed last month may bounce today. If a file stops working, [open an issue](../../issues) or send an updated version.

## 🤝 Contributing

PRs welcome — a good contribution:

1. **One prompt per file**, named `<model>.md` (lowercase, hyphens, no spaces for new files).
2. **Complete, not excerpted** — the full paste-ready prompt.
3. **Say where it goes** — system prompt, AGENTS.md, Modelfile, or config slot (the table's *Type* column).
4. **Version it honestly** — a revised prompt gets a new file (`opus v3.md`), not a silent overwrite.

Found a prompt that stopped working? An issue saying so is already useful.

## 📜 Disclaimer

All content is provided **for research and educational purposes only**, to document how prompt-level instruction conflicts surface in LLM behavior and to help builders harden their systems. The maintainers oppose using this material for any unlawful purpose and are not liable for misuse. Using these prompts may violate the terms of service of the models they target — that's on you, not us.

---

<div align="center">

**⭐ Star the repo if the collection saved you a session of prompt archaeology.**

*Issue reports and PRs keep this list alive — the models change, so the prompts must too.*

</div>
