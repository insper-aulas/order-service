# Order Service

Microservico Spring Boot responsavel por criacao e consulta de pedidos.

## Stack

- Java 21 / Spring Boot
- PostgreSQL com Flyway
- OpenFeign para Product Service e Exchange Service
- Prometheus via Spring Actuator

## Como executar

```bash
./mvnw spring-boot:run
```

Por padrao a aplicacao espera PostgreSQL e os servicos dependentes. Para subir tudo junto, use o compose do agregador:

```bash
cd ../micro_api_26.1
docker compose up --build order-service db product-service exchange-service
```

## Endpoints

- `POST /orders`
- `GET /orders`
- `GET /orders/{id}`

## Testes

```bash
./mvnw test
```

Os testes usam H2 em memoria e mocks para as dependencias externas.

## Documentacao

```bash
pip install -r requirements-docs.txt
mkdocs serve
```
