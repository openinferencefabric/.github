<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="oif-logo-dark-1200x400.png">
    <img src="oif-logo-light-1200x400.png" alt="Open Inference Fabric" width="660">
  </picture>
</p>

<p align="left"><b>Open source, bare metal to tokens: one platform to schedule, serve, benchmark and observe LLMs on NVIDIA and AMD GPUs.</b></p>

Website: **<https://openinferencefabric.github.io>**

**[oif](https://github.com/openinferencefabric/oif)** installs, with one command, a Kubernetes platform on GPU servers:
open-source NVIDIA Run:ai and the KAI Scheduler for projects, quotas and fractional GPUs, NVIDIA Dynamo for serving,
AIPerf for benchmarks, and Grafana dashboards for every GPU. NVIDIA and AMD GPUs run side by side in one cluster, and
every step has a tested guide. Apache-2.0.

### Upstream work: AMD GPUs in the open-source NVIDIA stack

Our changes go back to the upstream projects, not into private copies. Everything below is open for review.

| Project | What we sent |
| --- | --- |
| [Run:ai](https://github.com/dsx-ai-factory/run-ai) | PRs [#3950](https://github.com/dsx-ai-factory/run-ai/pull/3950) AMD GPUs in the node inventory · [#3948](https://github.com/dsx-ai-factory/run-ai/pull/3948) AMD icon for ROCm images · [#3949](https://github.com/dsx-ai-factory/run-ai/pull/3949) GPU fractions readiness; issue [#4274](https://github.com/dsx-ai-factory/run-ai/issues/4274) AMD GPU metrics |
| [KAI Scheduler](https://github.com/kai-scheduler/KAI-Scheduler) | PRs [#2557](https://github.com/kai-scheduler/KAI-Scheduler/pull/2557) reservation pod resources · [#2594](https://github.com/kai-scheduler/KAI-Scheduler/pull/2594) topology required level; design for AMD GPU fractions [#2556](https://github.com/kai-scheduler/KAI-Scheduler/issues/2556) |
| [KAI gpu-fractioning](https://github.com/kai-scheduler/gpu-fractioning) | PR [#175](https://github.com/kai-scheduler/gpu-fractioning/pull/175) hard VRAM limit per pod on AMD GPUs (Linux `dmem` cgroup) |
| [NVIDIA Dynamo](https://github.com/ai-dynamo/dynamo) | ROCm images for vLLM: co-developing [#12537](https://github.com/ai-dynamo/dynamo/pull/12537) (AMD) on branch [`rocm`](https://github.com/openinferencefabric/dynamo/tree/rocm), image builds on vLLM 0.33.0, benchmark on the Radeon PRO W7900 next |
| [ROCm](https://github.com/ROCm) | Issues [rocm-systems#14860](https://github.com/ROCm/rocm-systems/issues/14860) VRAM limits in `hipMemGetInfo` · [#14861](https://github.com/ROCm/rocm-systems/issues/14861) per-process GPU busy time · [device-metrics-exporter#722](https://github.com/ROCm/device-metrics-exporter/issues/722) per-pod metrics for shared GPUs |
| [KWOK](https://github.com/kubernetes-sigs/kwok) | Issue [#1802](https://github.com/kubernetes-sigs/kwok/issues/1802) AMD Instinct example nodes |

Every item, with lab evidence: [docs/UPSTREAM.md](https://github.com/openinferencefabric/oif/blob/main/docs/UPSTREAM.md) · live status: <https://openinferencefabric.github.io/upstream/>.

### Get involved

- **Test** on NVIDIA, AMD or mixed GPU servers and tell us what breaks.
- **Review** the upstream pull requests above, or try the Dynamo ROCm branch on your AMD GPU.
- **Contribute** Go, Kubernetes, ROCm/CUDA or docs: start with [CONTRIBUTING.md](https://github.com/openinferencefabric/oif/blob/main/CONTRIBUTING.md).
