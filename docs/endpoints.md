# Endpoints

Base URL in local compose: `http://localhost:8081`.

All order endpoints require the `id-account` header.

| Method | Path | Description |
| --- | --- | --- |
| `GET` | `/` | Health check |
| `POST` | `/orders` | Create an order |
| `GET` | `/orders` | List account orders |
| `GET` | `/orders/{id}` | Get order details |

## Create Order

```json
{
  "items": [
    {
      "idProduct": "8c4d22b7-1d6f-4bd4-b8fb-3f71b3853a84",
      "quantity": 2
    }
  ]
}
```

## Currency Conversion

```http
GET /orders/{id}?currency=BRL
id-account: 70
```
