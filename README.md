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



## Safra Bot API Service
Safra Bot é uma nova solução para o mercado de investimento, sugerindo investimos adqueados aos clientes baseado no perfil de investidor de cada um.

A api do safra bot tem como objetivo disponibilizar informações carteiras de investimento baseado no perfil do investidor

### Endpoints disponíveis 
URL Base: https://wlrfkvp3g5.execute-api.us-east-1.amazonaws.com/production/

suggetions:
https://wlrfkvp3g5.execute-api.us-east-1.amazonaws.com/production/safra-bot/v1/investment_suggestion/{client_id}

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

### Exemplo de Resposta - client id {00711234533}:
```
{
  "Suggestions": [
    {
      "Categoria": "Fundo Acoes",
      "NomeAtivo": [
        "SAFRA ACOES LIVRE FIC FIA",
        "SAFRA CONSUMO AMERICANO FIC AC",
        "SAFRA SELECTION FIC ACOES"
      ]
    },
    {
      "Categoria": "Fundos Imobiliarios",
      "NomeAtivo": [
        "HGLG11",
        "XPML11"
      ]
    }
  ]
}

```