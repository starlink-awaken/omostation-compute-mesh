# Compute Mesh

> eCOS 算力网格 — 算力发现、聚合、调度与 Worker 管理。

## 层位置

L1 运行时基础设施的算力抽象层：

```
L3 cockpit         ── 统一入口
L2 kairon          ── 知识引擎
L1 runtime         ── 运行时调度
L1 compute-mesh    ── 算力网格（本仓）
L0 ecos            ── 协议层
```

## 能力

- **算力发现** — 自动探测可用计算节点（本地/远程/云端）
- **算力聚合** — 统一资源视图，跨节点聚合 CPU/GPU/内存
- **调度分配** — 基于负载和优先级的任务分配
- **Worker 管理** — 生命周期管理、心跳监测、故障恢复

## Quick Start

```bash
uv sync
uv run pytest tests/ -q
```

## 依赖

- Python >=3.10
- uv 包管理器
