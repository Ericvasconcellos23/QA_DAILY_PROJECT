# US-001 — Login do Usuário

## História de Usuário

**Como** cliente cadastrado  
**Quero** realizar login utilizando meu e-mail e senha  
**Para** acessar minha conta e utilizar as funcionalidades do sistema.

## Critérios de Aceite

- CA01: Usuário com e-mail e senha válidos deve conseguir entrar no sistema.
- CA02: Usuário com senha incorreta não deve conseguir entrar.
- CA03: Usuário com e-mail não cadastrado não deve conseguir entrar.
- CA04: E-mail é obrigatório.
- CA05: Senha é obrigatória.
- CA06: Após login bem-sucedido, o usuário deve ser direcionado para a página inicial.

## Regras definidas no refinamento

- Credenciais inválidas devem exibir: `E-mail ou senha inválidos.`
- E-mails não diferenciam letras maiúsculas e minúsculas.
- Espaços antes ou depois do e-mail devem ser desconsiderados.
- E-mail em formato inválido deve exibir: `Informe um e-mail válido.`
- Campos obrigatórios vazios devem exibir: `Campo obrigatório.`

## Cenários de Teste

### Cenário 01 — Login com credenciais válidas

**Dado** que o usuário já esteja cadastrado no sistema  
**E** esteja na página de login  

**Quando** preencher o campo e-mail com um e-mail válido  
**E** preencher o campo senha com a senha correta  
**E** clicar no botão "Entrar"  

**Então** o login deve ser realizado com sucesso  
**E** o usuário deve ser direcionado para a página inicial


### Cenário 02 — Login com senha incorreta

**Dado** que o usuário esteja cadastrado no sistema  
**E** esteja na página de login  

**Quando** preencher o campo e-mail com um e-mail cadastrado  
**E** preencher o campo senha com uma senha incorreta  
**E** clicar no botão "Entrar"  

**Então** o login não deve ser realizado  
**E** deve ser exibida a mensagem "E-mail ou senha inválidos."

### Cenário 03 — Login com e-mail não cadastrado

**Dado** que o usuário não esteja cadastrado no sistema
**E** esteja na página de login

**Quando** preencher o campo e-mail com um e-mail não cadastrado
**E** preencher o campo senha com uma senha válida 
**E** clicar no botão "Entrar"

**Então** o login não deve ser realizado
**E** deve ser exibida a mensagem "E-mail ou senha inválidos"

### Cenário 04 — Campo e-mail vazio

**Dado** que o usuário esteja na página de login

**Quando** deixar o campo e-mail vazio  
**E** preencher o campo senha com uma senha válida  
**E** clicar no botão "Entrar"

**Então** o login não deve ser realizado  
**E** deve ser exibida a mensagem "Campo obrigatório."


### Cenário 05 — Campo senha vazio

**Dado** que o usuário esteja na página de login

**Quando** preencher o campo e-mail com um e-mail válido  
**E** deixar o campo senha vazio  
**E** clicar no botão "Entrar"

**Então** o login não deve ser realizado  
**E** deve ser exibida a mensagem "Campo obrigatório."