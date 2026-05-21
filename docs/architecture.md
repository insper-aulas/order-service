# Architecture

```mermaid
flowchart LR
    Client[Gateway] --> Resource[Order Resource]
    Resource --> Service[Order Service]
    Service --> Product[Product Service]
    Service --> Exchange[Exchange Service]
    Service --> Repository[Order Repository]
    Repository --> Database[(PostgreSQL)]
```

## Persistence

Flyway creates the `orders` schema with `orders.orders` and `orders.order_items`.

## Service Calls

OpenFeign clients call Product Service and Exchange Service using URLs injected through `PRODUCT_SERVICE_URL` and `EXCHANGE_SERVICE_URL`.
