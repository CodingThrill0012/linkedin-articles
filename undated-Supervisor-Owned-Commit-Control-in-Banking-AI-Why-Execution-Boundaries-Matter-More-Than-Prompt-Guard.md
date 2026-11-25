---
title: "Supervisor-Owned Commit Control in Banking AI: Why Execution Boundaries Matter More Than Prompt Guardrails"
date: undated
source: LinkedIn Articles
author: Divyendu Bhatt
---

# Supervisor-Owned Commit Control in Banking AI: Why Execution Boundaries Matter More Than Prompt Guardrails

![](https://media.licdn.com/mediaD5612AQFJbuARw9Y4GQ)

# [Supervisor-Owned Commit Control in Banking AI: Why Execution Boundaries Matter More Than Prompt Guardrails](https://www.linkedin.com/pulse/supervisor-owned-commit-control-banking-ai-why-execution-dm-bhatt-mucjc)

Created on 2026-11-24 07:40

Published on 2026-11-24 07:53

<div>

When banks deploy AI agents for transfer assistants, limit reviews, or dispute handling, two groups feel the tension immediately: **Product Developers** need fast, composable multi-agent workflows, while **CISOs** need hard guarantees that an agent cannot silently mutate regulated state or trigger unauthorized payments.

Relying on prompt instructions or model alignment does not satisfy either requirement. In **Yama** ( / ), we separate **agent reasoning** from **durable side-effects** using a supervisor-owned commit path.

### The Architecture in 4 Steps

1.  **Scoped Grant at Intent:** When a customer authenticates and states intent, the control plane issues a time-bound (e.g., , , ).

2.  **Restrained Agent Execution:** The analysis agent reads context and emits proposals tagged with (, , , ). The agent process itself has no write access to payment instructions or core-banking endpoints.

3.  **Commit-Time Re-Validation:** Immediately before durable write or API dispatch, the supervisor re-checks grant validity, revocation state, purpose binding, and trust level inside .

4.  **Deterministic Refusal or Auditable Commit:** Any drift—such as a customer cancel, fraud revocation, or mismatch—raises before a file or transaction exists. Valid commits write the instruction and log alongside the full provenance payload.

### What Developers & CISOs Should Watch in Production

Security architectures earn trust by measuring their boundaries rather than assuming them:

-   **Residual TOCTOU Window:** Even with a check immediately preceding the write, a revocation arriving between check return and durable write will not be caught by that check. In localhost benchmarks (), that window measured a median of **0.001498 s** and max **0.002449 s**—a concrete metric teams must bound alongside revocation propagation latency.

-   **OS-Level Containment:** In baseline attack tests, filesystem Landlock blocked out-of-scope file writes and denied binary execution (, ), but left outbound TCP () open when was false. Closing direct network egress from agent workers requires **Landlock ABI ≥ 4 TCP-connect rules** or **seccomp-BPF**.

-   **Scope Clarity:** Provenance and commit checks enforce *authority and attribution*, not semantic truth—prompt injection inside an authorized payload and post-commit settlement reversals remain separate control layers.

### Explore & Collaborate

I am actively expanding Yama’s kernel restraint benchmarks ( + Landlock TCP rules) and multi-agent revocation semantics. Review the runnable example, sample JSON contracts, and benchmark logs here:

If you are architecting AI control planes in banking or financial infrastructure, I’d value your perspective on where commit-time enforcement and OS sandboxing fit in your stack.

</div>