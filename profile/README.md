# EvalHub

**Open source evaluation orchestration for AI systems.**

EvalHub is a platform for running systematic evaluations of models, agents, and AI systems across multiple frameworks, without locking you into any single one.

Run evaluations against any registered benchmark, whether built-in or one you create yourself, track experiments in MLflow, and store immutable results as OCI artefacts.

It works locally for development and scales on Kubernetes for production.

## Repositories

| Repository | Description |
|------------|-------------|
| [`eval-hub`](https://github.com/eval-hub/eval-hub) | Go REST API server — evaluation orchestration, provider registry, benchmark discovery, collection management |
| [`eval-hub-sdk`](https://github.com/eval-hub/eval-hub-sdk) | Python SDK — async/sync clients, adapter framework (BYOF), CLI tools, MCP server for agent integration |
| [`eval-hub-contrib`](https://github.com/eval-hub/eval-hub-contrib) | Community-contributed framework adapters (LightEval, GuideLLM, MTEB, and more) |
| [`eval-hub.github.io`](https://github.com/eval-hub/eval-hub.github.io) | Documentation site — architecture, guides, SDK reference |

## Key capabilities

- **Versioned REST API** (v1) with OpenAPI specification and interactive docs
- **Provider registry** with benchmark discovery and category filtering
- **Benchmark collections** with weighted scoring and compliance requirements
- **Bring Your Own Framework** implement a single method to add any evaluation framework
- **Kubernetes-native** job orchestration with resource isolation
- **MLflow integration** for experiment tracking, lineage, and result comparison
- **OCI artefact persistence** for reproducible, immutable evaluation results
- **Multi-provider batching** groups compatible benchmarks to reduce execution time
- **Prometheus metrics** and OpenTelemetry tracing

## Supported adapters

| Adapter | What it evaluates |
|---------|-------------------|
| **lm-eval-harness** | 167 benchmarks across 12 categories (reasoning, math, science, safety, ...) |
| **LightEval** | Accuracy, normalised accuracy, exact match |
| **GuideLLM** | TTFT, ITL, throughput, latency |
| **MTEB** | Semantic similarity, retrieval, classification |
| **Garak** | OWASP Top 10, vulnerability scanning, safety probes |

## Documentation

Full documentation is available at [eval-hub.github.io](https://eval-hub.github.io):

- [Overview](https://eval-hub.github.io/getting-started/overview/) — architecture and core concepts
- [Installation](https://eval-hub.github.io/getting-started/installation/) — install server and SDK
- [Quick start](https://eval-hub.github.io/getting-started/quickstart/) — run your first evaluation
- [Python SDK reference](https://eval-hub.github.io/reference/sdk-client/) — client and adapter API
- [Building adapters](https://eval-hub.github.io/adapters/) — create your own framework adapter

## Licence

Apache 2.0 — see [LICENCE](https://github.com/eval-hub/eval-hub/blob/main/LICENSE).
