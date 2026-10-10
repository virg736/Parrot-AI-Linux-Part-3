

<h2 align="center">🛡️ AI Agent Security & Red Team Testing 🛡️</h2>

<p align="center">
  <strong>Securing a Local AI Agent with Qwen3 and a Deterministic Policy Engine</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Linux-Parrot%20OS-00BFA5?style=flat-square">
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=flat-square">
  <img src="https://img.shields.io/badge/LLM-Qwen3-purple?style=flat-square">
  <img src="https://img.shields.io/badge/Inference-llama.cpp-green?style=flat-square">
  <img src="https://img.shields.io/badge/Testing-pytest-orange?style=flat-square">
  <img src="https://img.shields.io/badge/Security-Policy%20Engine-red?style=flat-square">
  <img src="https://img.shields.io/badge/Red%20Team-100%20Scenarios-blueviolet?style=flat-square">
</p>

<p align="center">
  This third part of Parrot AI Linux focuses on strengthening the security of a local AI agent through automated testing and adversarial Red Team scenarios.
</p>

<h2 align="center">🎥 Watch the Full Video on YouTube 🎥</h2>

<p align="center">
  <a href="https://www.youtube.com/watch?v=V7P1GnN_tMY">
    <img src="https://img.youtube.com/vi/V7P1GnN_tMY/maxresdefault.jpg"
         alt="I Tested My Linux AI Agent with 100 Red Team Scenarios"
         width="700">
  </a>
</p>


---

  This third part of Parrot AI Linux focuses on strengthening the security of a local AI agent through automated testing and adversarial Red Team scenarios.
</p>

---

## 🛠️ Tech Stack

`Linux` · `Parrot OS` · `Python` · `Qwen3` · `llama.cpp` · `pytest` · `Pydantic` · `Git` · `Policy Engine`

- **Parrot Security OS** — Linux development and testing environment
- **Python** — AI agent logic and security controls
- **Qwen3** — local language model
- **llama.cpp** — local LLM inference
- **Pydantic** — structured data validation
- **pytest** — automated security regression tests
- **Policy Engine** — deterministic ALLOW / DENY / CLARIFY decisions
- **Git** — version control

---

## 🔐 Core Principle

> **The LLM proposes. The Policy Engine decides. Linux executes only what is allowed.**

The architecture separates AI-generated proposals from actual Linux command execution.

Security controls evaluate each proposed action before execution.

---

## Red Team Security Testing

The AI agent was evaluated using 100 Red Team scenarios designed to test its security boundaries and decision-making behavior.

### Test Results

| Decision | Results |
|:---|---:|
| Total scenarios | 100 |
| DENY | 43 |
| CLARIFY | 55 |
| ALLOW | 2 |
| API errors | 0 |

### 🔎 Key Finding

Two scenarios resulted in ALLOW decisions involving the authorized `whoami` command.

This highlights an important security consideration:

> **Allowing a command is not enough. An AI agent's actions must also align with the user's original intent.**

These findings identify a potential security risk requiring further testing.

---

### AI Defender vs. AI Attacker

The next phase will introduce two AI agents:

- **AI Defender** - protects the Linux environment through security policies
- **AI Attacker** - evaluates the defender through controlled adversarial scenarios

The objective is to strengthen security controls and expand Red Team testing.

---

## 📝 Note

This repository documents the architecture, development, security testing, and evolution of Parrot AI Linux.

The complete source code remains private to protect the project's implementation and security-sensitive logic.

Technical demonstrations and selected development results are shared publicly for professional presentation and portfolio purposes.

<p align="center">
  © 2026 Virginie Lechene
</p>


