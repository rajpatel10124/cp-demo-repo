# python-api Architecture & Documentation

Welcome to the documentation for background worker **python-api**.

## Architecture & Queue Consumer Flow

```
Event Stream / Queue ──> Poller ──> Worker Concurrency Pool (5 threads) ──> Prometheus Metrics (Port 9090)
```

## Operation & Monitoring

- **Concurrency**: `5` parallel job executions.
- **Health Probes**: `GET http://localhost:9090/healthz`
- **Metrics**: `GET http://localhost:9090/metrics`
