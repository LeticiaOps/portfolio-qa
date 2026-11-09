# API

# Testes de API com Postman

Collection com requests e testes automáticos (aba After response) contra dois sites públicos de treino: JSONPlaceholder e Restful-booker.

## Como usar
1. No Postman, clique em Import e selecione `QA portfolio.postman_collection.json`.
2. (Opcional) Importe também o arquivo de environment, que define a variável `baseUrl`.
3. Clique nos três pontinhos da collection e em Run collection para rodar tudo.

## O que foi testado

### JSONPlaceholder
| Request | Esperado | Obtido |
|---|---|---|
| GET - Buscar post 1 | 200, campo `title`, resposta rápida | 200 |
| GET - Posts do usuário 1 | 200 e lista só com posts do usuário 1 | 200 |
| POST - Criar post | 201 e título enviado devolvido | 201 |
| PUT - Atualizar post | 200 | 200 |
| DELETE - Apagar post | 200 | 200 |
| GET - Post inexistente | 404 | 404 |

### Restful-booker
| Request | Esperado | Obtido |
|---|---|---|
| POST - Autenticar (token) | 200 e campo `token` | 200 |
| POST - Criar reserva | 200 e `bookingid` | 200 |
| PUT - Atualizar reserva (com token) | 200 | 200 |
| PUT - Sem token | 403 | 403 |

## Conceitos praticados
- Métodos HTTP: GET, POST, PUT e DELETE
- Query params (`/posts?userId=1`) e path params (`/posts/1`)
- Status codes: 200, 201, 403, 404 e 405
- Autenticação com token (header `Cookie`)
- Testes automáticos: status, campos do JSON e tempo de resposta
- Variáveis e environment (`baseUrl`)

## Observações
- Em uma execução, o PUT em `/booking/{id}` retornou 405. O id da reserva não existia mais, porque o site de treino apaga dados periodicamente. Ao criar uma reserva nova e repetir os passos em sequência, retornou 200.
- O Restful-booker é um site público e pode ficar instável. Se algum teste falhar, vale rodar de novo.
- As credenciais usadas (`admin` / `password123`) são públicas e de treino. Em projeto real, nunca suba senhas ou tokens para o repositório.

## Evidência
Resultado do Collection Runner: `runner-resultado.png`
