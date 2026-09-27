# Casos de Teste — US-001 Login

## CT-001 — Login com credenciais válidas

**Requisito relacionado:** CA01 / CA06

**Pré-condições:**
- Usuário deve estar cadastrado e ativo no sistema.
- Sistema deve estar disponível para testes.

**Dados de teste:**
- E-mail: usuário válido cadastrado
- Senha: senha válida correspondente ao usuário

**Passos:**
1. Acessar a página de login.
2. Preencher o campo e-mail com um e-mail válido.
3. Preencher o campo senha com a senha correta.
4. Clicar no botão "Entrar".

**Resultado esperado:**
- Login realizado com sucesso.
- Usuário direcionado para a página inicial.

**Status:** Não executado


## CT-002 — Login com senha incorreta

**Requisito relacionado:** CA02 


**Pré-condições:**
- Usuário deve estar cadastrado e ativo no sistema.
- Sistema deve estar disponível para testes.

**Dados de teste:**
- E-mail: usuário válido cadastrado
- Senha: senha incorreta para o usuário informado.

**Passos:**
1. Acessar a página de login.
2. Preencher o campo e-mail com um e-mail válido.
3. Preencher o campo senha com a senha incorreta.
4. Clicar no botão "Entrar".

**Resultado esperado:**
- Login não deve ser realizado.
- Deve ser exibida a mensagem "E-mail ou senha inválidos."
- Usuário permanece na página de login.

**Status:** Não executado


## CT-003 — Login com e-mail não cadastrado

**Requisito relacionado:** CA03

**Pré-condições:**
- O e-mail utilizado no teste não deve estar cadastrado no sistema.
- Sistema deve estar disponível para testes.

**Dados de teste:**
- E-mail: e-mail válido em formato, porém não cadastrado.
- Senha: senha válida em formato.

**Passos:**
1. Acessar a página de login.
2. Preencher o campo e-mail com um e-mail não cadastrado.
3. Preencher o campo senha com uma senha válida.
4. Clicar no botão "Entrar".

**Resultado esperado:**
- Login não deve ser realizado.
- Deve ser exibida a mensagem "E-mail ou senha inválidos."
- Usuário deve permanecer na página de login.

**Status:** Não executado

## CT-004 — Campo e-mail vazio

**Requisito relacionado:** CA04

**Pré-condições:**
- Sistema deve estar disponível para testes.
- Usuário deve estar na página de login.

**Dados de teste:**
- E-mail: não preencher.
- Senha: senha válida.

**Passos:**
1. Acessar a página de login.
2. Deixar o campo e-mail vazio.
3. Preencher o campo senha com uma senha válida.
4. Clicar no botão "Entrar".

**Resultado esperado:**
- Login não deve ser realizado.
- Deve ser exibida a mensagem "Campo obrigatório."
- Usuário deve permanecer na página de login.

**Status:** Não executado


## CT-005 — Campo senha vazio

**Requisito relacionado:** CA05

**Pré-condições:**
- Usuário deve estar cadastrado e ativo no sistema.
- Sistema deve estar disponível para testes.

**Dados de teste:**
- E-mail: e-mail válido cadastrado.
- Senha: não preencher.

**Passos:**
1. Acessar a página de login.
2. Preencher o campo e-mail com um e-mail válido cadastrado.
3. Deixar o campo senha vazio.
4. Clicar no botão "Entrar".

**Resultado esperado:**
- Login não deve ser realizado.
- Deve ser exibida a mensagem "Campo obrigatório."
- Usuário deve permanecer na página de login.

**Status:** Não executado