# Safra Tecnee - Invest Plus | Safra Bot - Services

## Invest Plus API Service
Invest Plus é uma nova solução para o mercado de investimento.

A api do invest plus tem como objetivo disponibilizar informações sobre:
- Cliente
- Carteira de investimento do cliente

### Endpoints disponíveis 
URL Base: https://wlrfkvp3g5.execute-api.us-east-1.amazonaws.com/production/

all accounts:
https://wlrfkvp3g5.execute-api.us-east-1.amazonaws.com/production/invest-plus/v1/accounts

client account:
https://wlrfkvp3g5.execute-api.us-east-1.amazonaws.com/production/invest-plus/v1/accounts/{client_id}

all wallets:
https://wlrfkvp3g5.execute-api.us-east-1.amazonaws.com/production/invest-plus/v1/wallets

client wallet:
https://wlrfkvp3g5.execute-api.us-east-1.amazonaws.com/production/invest-plus/v1/wallets/{client_id}

### Requisição

Esses endpoints respondem ao metodo GET;
no Header da requisição é preciso informar um token:
```
Authorization: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJuYW1lIjoic2FmcmEtc2VjcmV0IiwianRpIjoiMTcwNjBkMzktZTc3Yi00Y2YxLTgxYWUtNGY4MmM0ODg3NjMxIiwiaWF0IjoxNTk5ODgyNDI2LCJleHAiOjE1OTk4ODYwMjZ9.f-LhhN5uLcpVCGldireDayaAJsfSWhYlxI11wAinIac
```
Os client_id disponíveis são:
- 00711234511
- 00711234522
- 00711234533

### Exemplo de Resposta - client id {00711234522}:
```
{
  "Accounts": [
    {
      "AccountId": "00711234522",
      "Currency": "BRL",
      "Nickname": "Satya",
      "Name": "Satya Nadella da Silva",
      "Identification": "12345678901222",
      "Age": "28",
      "Investor": "1",
      "InvestorProfile": "Moderado",
      "Amount": "800",
      "PorcentagemAcoes": "50",
      "PorcentagemFIIs": "50",
      "SafraCoins": "30"
    }
  ]
}
```