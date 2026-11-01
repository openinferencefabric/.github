<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="oif-logo-dark-1200x400.png">
    <img src="oif-logo-light-1200x400.png" alt="Open Inference Fabric" width="440">
  </picture>
</p>

<p align="left"><b>Open source, bare metal to tokens: one platform to schedule, serve, benchmark and observe LLMs on NVIDIA and AMD GPUs.</b></p>

**[oif](https://github.com/openinferencefabric/oif)** installs, with one command, a Kubernetes platform on GPU servers:
open-source NVIDIA Run:ai and the KAI Scheduler for projects, quotas and fractional GPUs, NVIDIA Dynamo for serving,
AIPerf for benchmarks, and Grafana dashboards for every GPU. NVIDIA and AMD GPUs run side by side in one cluster, and
every step has a tested guide. Apache-2.0.

### Upstream work: AMD GPUs in Run:ai and the KAI Scheduler

| Project | Pull requests (under review) |
| --- | --- |
| [Run:ai](https://github.com/dsx-ai-factory/run-ai) | [#3950](https://github.com/dsx-ai-factory/run-ai/pull/3950) AMD GPUs in the node inventory · [#3948](https://github.com/dsx-ai-factory/run-ai/pull/3948) AMD icon for ROCm images · [#3949](https://github.com/dsx-ai-factory/run-ai/pull/3949) GPU fractions readiness |
| [KAI Scheduler](https://github.com/kai-scheduler/KAI-Scheduler) | [#2557](https://github.com/kai-scheduler/KAI-Scheduler/pull/2557) reservation pod resources |

Issues with lab evidence and the full list: [docs/UPSTREAM.md](https://github.com/openinferencefabric/oif/blob/main/docs/UPSTREAM.md).

### Get involved

- **Test** on NVIDIA, AMD or mixed GPU servers and tell us what breaks.
- **Review** the upstream pull requests above.
- **Contribute** Go, Kubernetes, ROCm/CUDA or docs: start with [CONTRIBUTING.md](https://github.com/openinferencefabric/oif/blob/main/CONTRIBUTING.md).
