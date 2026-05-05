# Brutal Programming: The 10x Architect Manifesto

**"Complexity is the enemy. Autonomy is the solution. Precision is the result."**

## What is Brutal Programming?
**Brutal Programming** is an AI-native development methodology designed for the senior engineer who orchestrates intelligence rather than just writing code. 

In an era of AI hallucinations and "lazy coding," Brutal Programming focuses on **Raw Output, Independent Validation, and Zero Fluff.** It is inspired by Brutalist architecture: functional, structural, and unapologetically honest.

---

## Core Pillar: Independent Dual-Agent Validation (IDAV)
The biggest failure in modern AI coding is staying in a single chat thread. If an AI makes a mistake, it will often "hallucinate a fix" based on its own previous error. 

**Brutal Programming mandates a split-brain approach:**

### 1. The Architect (Primary Agent)
*   **Role:** Generates the logic, the RAG orchestration, and the core implementation.
*   **Context:** Deeply embedded in the project requirements.

### 2. The Adversary (Independent Agent)
*   **Role:** A completely separate AI instance (different provider or fresh thread) with **zero** knowledge of the Architect's thought process.
*   **Context:** Receives only the *output* and the *specification*.
*   **Task:** To break, critique, and find edge cases in the Architect’s code.

---

## The "Brutal Orchestrator" System Prompt
To implement this, I use a specific meta-prompting strategy. This prompt is used to turn a high-reasoning LLM into an **Orchestrator** that manages a terminal-based **Executor** (like Claude Code or Replit Agent).[cite: 1]

### The Rules of Orchestration:
*   **Mode: Planning:** The Executor is never allowed to modify files until a blueprint is approved.[cite: 1]
*   **The "GO" Protocol:** Implementation happens in atomic steps. No "all-in-one" pushes. Every step requires a manual "GO".[cite: 1]
*   **Verification-First:** Every implementation must include unit tests, lints, and log analysis (e.g., FastAPI logs) before being considered "Done".[cite: 1]
*   **Git Discipline:** Mandatory commits after every successful logical unit to ensure a clean, reversible history.[cite: 1]

---

## Proven Implementations
This methodology isn't theoretical. It has been used to build:

*   **VertigoLaw / Vertigogo:** Transforming 16,000 inconsistent documents into structured RAG databases.
*   **Multi-Tenant Systems:** Managing migrations and logic across isolated tenant databases with zero cross-contamination.[cite: 1]
*   **Automated Security Audits:** Using the "Adversary Agent" to perform real-time security reviews of generated code.

---

## Philosophy
> "I don't write code anymore. I orchestrate intelligence. I am the Architect of a system that builds itself, validated by a system that tries to break it."

---

## Repository Structure
*   `/orchestration`: Contains the "Brutal Orchestrator" system prompts.
*   `/examples`: Boilerplate projects built using the IDAV workflow.
*   `/docs`: Deep dives into AI-native CI/CD and testing.

---
© 2026 | Developed by Cornelii Sandberg
