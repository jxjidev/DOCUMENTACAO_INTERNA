# 7DEWZWP8K

````
# API de Pagamentos

## Visao Geral

Essa API permite processar pagamentos de forma segura e eficiente.

## Endpoints

### POST /payments

Cria um novo pagamento.

**Request Body:**

```json
{
  "amount": 100,
  "currency": "BRL"
}
```

**Response:**

| Campo | Tipo | Descricao |
|-------|------|-----------|
| id | string | ID do pagamento |
| status | string | Status: pending, approved, rejected |
| created_at | datetime | Data de criacao |

## Exemplo de Uso

```csharp
var payment = await api.CreatePayment(new PaymentRequest
{
    Amount = 100,
    Currency = "BRL"
});
```
````
