# Misinformation Detection Agent System – Pitch

## Core Concept & Value

Misinformation and disinformation are now ranked as the **#1 short‑term global risk** by the World Economic Forum. False claims about health, climate, elections, and public policy travel faster than ever, while manual fact‑checking cannot keep up. Individuals, journalists, and platform moderators need something better than ad‑hoc Googling: they need **reliable, explainable, and repeatable** help to decide, “Can I trust this content?”

This project builds a **multi‑agent misinformation detection system** that combines several complementary skills:

- A **Content Analyzer** that extracts verifiable claims and emotional/bias signals.
- A **Fact Checker** that verifies each claim against multiple sources in parallel.
- A **Source Verifier** that evaluates publisher credibility and bias.
- An **Orchestrator** that synthesizes a final verdict and credibility score.

The system outputs a clear verdict (**TRUE / FALSE / MISLEADING / UNCERTAIN**), a numeric credibility score, a risk level, and concise reasoning. The goal is not only to say “this is false,” but to show *why* and *based on which evidence*.

## Track Alignment – Agents for Good

This project is submitted under the **Agents for Good** track. It directly addresses the societal harm caused by misinformation:

- **Public Health** – harmful myths about vaccines and medicine.
- **Climate & Environment** – denial of scientific consensus.
- **Democracy & Policy** – conspiracy narratives that erode institutional trust.

By using agents to scale and explain misinformation detection, the project aims to **support healthier information ecosystems**, empower users to question dubious claims, and give platforms a starting point for moderation workflows.

## Why Agents?

Misinformation detection is inherently **multi‑step and multi‑skill**:

1. Understand the content and extract claims.
2. Search for and retrieve potential evidence.
3. Evaluate the credibility of sources.
4. Combine everything into a human‑readable verdict.

A single model call is not enough. The multi‑agent design makes the system:

- **Modular** – each agent focuses on a well‑defined role.
- **Explainable** – each stage leaves a trace (claims found, sources used, reasoning).
- **Extensible** – new tools (e.g. domain‑specific fact APIs) can be plugged in easily.

## Value Proposition

- For **end users**: a one‑shot verdict with explanations and (when possible) linked citations.
- For **developers**: a reusable, production‑styled detector class (`RateLimitedDetector`) with clear APIs, rate limiting, observability, and deployment examples.
- For **researchers and educators**: a concrete example of how to turn LLMs + tools + agents into a real, multi‑step decision system, not just a chat interface.