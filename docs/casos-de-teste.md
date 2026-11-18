# Casos de teste: Login (SauceDemo)

Site: https://www.saucedemo.com | Ambiente: Chrome

| ID | Título | Passos | Resultado esperado | Obtido |
|---|---|---|---|---|
| CT01 | Login com credenciais válidas | 1. Abrir o site. 2. Usuário `standard_user`. 3. Senha `secret_sauce`. 4. Clicar em Login. | Abre a página de produtos (Products) | Login realizado com sucesso. Abriu a página de Produtos. ☑️ |
| CT02 | Login com senha inválida | 1. Abrir o site. 2. Usuário `standard_user`. 3. Senha `errada`. 4. Clicar em Login. | Mensagem de erro de usuário e senha que não correspondem | Login com senha incorreta resultou em mensagem de erro de dados que não são válidos. ☑️ |
| CT03 | Login com usuário bloqueado | 1. Abrir o site. 2. Usuário `locked_out_user`. 3. Senha `secret_sauce`. 4. Clicar em Login. | Mensagem informando que o usuário foi bloqueado | Login com user bloqueado trouxe a mensagem de "Epic sadface: Sorry, this user has been locked out." ☑️  |
| CT04 | Login sem informar usuário | 1. Abrir o site. 2. Deixar usuário vazio. 3. Senha `secret_sauce`. 4. Clicar em Login. | Mensagem de que o usuário é obrigatório | Login sem inserção de dado de usuário resultou em mensagem de erro "Epic sadface: Username is required" ☑️ |
| CT05 | Login sem informar senha | 1. Abrir o site. 2. Usuário `standard_user`. 3. Deixar senha vazia. 4. Clicar em Login. | Mensagem de que a senha é obrigatória | Login sem inserção de senha resultou em mensagem de erro  "Epic sadface: Password is required" ☑️ |