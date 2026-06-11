# AGENTS.md — Compute Mesh

> eCOS v5 算力网格 · 计算发现 + 资源聚合 + 任务调度 + Worker 生命周期

## Quick Commands

```bash
cd projects/compute-mesh
uv run pytest tests/ -q
uv run ruff check src/
```

## Architecture

L1 运行时基础设施的算力抽象层：

```
L3 cockpit        ── 统一入口
L1 runtime        ── 运行时调度
L1 compute-mesh   ── 算力网格（本仓）
```

### 能力

- **计算发现** — 自动探测可用计算节点
- **算力聚合** — 统一资源视图 (CPU/GPU/内存)
- **调度分配** — 基于负载和优先级的任务分配
- **Worker 管理** — 生命周期 + 心跳 + 故障恢复

## Dependencies

- Python >=3.10, uv

## Testing

```bash
uv run pytest tests/ -q
```
