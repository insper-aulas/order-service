# Bottlenecks

Order creation depends on Product Service availability. Currency conversion also depends on Exchange Service when the client requests a currency different from USD.

## Mitigations

- Short HTTP timeouts on OpenFeign.
- Defensive error mapping for unavailable dependencies.
- Kubernetes HPA for CPU-based scale-out.
- PostgreSQL schema managed by Flyway to keep deployments repeatable.
