# Order Service

The Order Service creates and lists authenticated customer orders.

It persists order data in PostgreSQL, validates products by calling Product Service and converts totals through Exchange Service when a different currency is requested.

## Responsibilities

- Create orders for the current account.
- Store order items and totals.
- List only orders that belong to the current account.
- Convert order totals using the Exchange API.
