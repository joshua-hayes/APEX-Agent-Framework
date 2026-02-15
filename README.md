## Overview

APEX follows a simple but powerful architecture:

- **Planner (LLM)** – Gathers information, reasons about missing fields, and prepares structured input.
- **Executor (Backend)** – A deterministic C# API that validates inputs and renders templates.
- **Verifier (Validator)** – Ensures required fields are present and correctly formatted.
- **Control Loop** – Iteratively corrects errors until validation passes.

The framework integrates with Microsoft 365 Copilot and Teams via an OpenAPI‑based plugin, enabling conversational workflows for generating engineering documentation.

## Project Goals

- Provide a reusable, open‑source agentic automation pattern.
- Enable consistent, validated engineering documents.
- Demonstrate hybrid LLM + backend orchestration.
- Integrate with Microsoft Teams and Copilot.
- Serve as a foundation for more advanced agentic systems (retrieval, knowledge graphs, multi‑agent workflows).

## v0.1 Scope (Current Version)

The initial version focuses on the smallest possible working end‑to‑end system:

- C# minimal API backend
- One document type: **RCA**
- RCA model and validation rules
- RCA markdown template
- `/validate-rca` endpoint
- `/generate-rca` endpoint
- Template rendering engine
- Auto‑generated OpenAPI specification
- Copilot plugin manifest for manual testing
