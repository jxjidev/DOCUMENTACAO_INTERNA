# 3CRVLV6KE

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

## Exemplo de Uso

```csharp
var payment = await api.CreatePayment(new PaymentRequest
{
    Amount = 100,
    Currency = "BRL"
});
```
````
