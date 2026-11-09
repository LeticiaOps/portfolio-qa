# API

# Testes de API com Postman

Collection com requests e testes automáticos (aba After response) contra dois sites públicos de treino.

## Como usar
1. No Postman: Import → selecione `QA-portfolio.postman_collection.json`
2. Clique em Run collection para rodar tudo.

## O que foi testado
| Request | Esperado | Obtido |
|---|---|---|
| GET - Buscar post 1 | 200 e campo title | |
| GET - Posts do usuário 1 | 200 e só posts do usuário 1 | |
| POST - Criar post | 201 | |
| PUT - Atualizar post | 200 | |
| DELETE - Apagar post | 200 | |
| GET - Post inexistente | 404 | |
| POST - Autenticar (token) | 200 e campo token | |
| PUT - Atualizar reserva (com token) | 200 | |
| PUT - Sem token | 403 | |

## Observações
- (cole aqui a anotação do 405 que você fez)

## Evidência
Resultado do Collection Runner: `runner-resultado.png`
