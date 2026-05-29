# Agentic Software Engineering: Practical Patterns for Enterprise Teams


## Common Failure Modes

1. Context Window Collapse
2. No Architectural Constraints
3. Verification Blindness
4. Unsafe MCP Usage
5. Tool Overload
6. “One-Shot Agent” Anti-Pattern


## Context Window Collapse

What is context window ?

What all is loaded during start of a session ?

Context Rot ?

How existing Model itself hadles this 

Room for further improvemtns improvement 

Imagine a developer using an AI coding assistant for 3 hours continuously.

The prompt history now contains:

  requirements,
  half-finished implementations,
  old decisions,
  rejected approaches,
  logs,
  stack traces,
  temporary experiments,
  conflicting instructions,
  copied documentation,
  previous bugs,
  architectural discussions,
  generated code.

Eventually the model starts to:

  forget original constraints,
  contradict earlier design decisions,
  reintroduce deleted bugs,
  generate inconsistent APIs,
  hallucinate nonexistent abstractions,
  mix old and new architectures,
  ignore coding standards,
  produce unstable reasoning.

That degradation is what teams informally call:

  context collapse,
  context rot,
  prompt drift,
  long-context degradation,
  attention collapse.


## “Context Engineering” > Prompt Engineering

First rule of LLMS --> write better prompt. But is it enought for enterprise application. Probabaly no. It much more . Let see

  - Context Control
  - Tool orchestration
  - retrieval
  - memory
  - 





A comprehensive guide to Large Language Models (LLMs).

## Overview

This repository contains resources, documentation, and guides about Large Language Models, their applications, best practices, and implementation strategies.

## Contents

- Documentation and tutorials
- Best practices and patterns
- Examples and use cases
- Resources and references

## Getting Started

To get started with this guide, explore the documentation files and examples provided in this repository.

## Contributing

Contributions are welcome! Feel free to submit issues and pull requests to improve this guide.

## License

## Reference 
Lost in Middle - https://huggingface.co/papers/2307.03172?utm_source=chatgpt.com
https://arxiv.org/abs/2403.04797?utm_source=chatgpt.com
https://arxiv.org/abs/2412.10079?utm_source=chatgpt.com
Reddit - https://www.reddit.com/r/ContextEngineering/comments/1pclw66/context_engineering_for_agents_what_actually_works/?utm_source=chatgpt.com


For questions or feedback, please open an issue in this repository.
