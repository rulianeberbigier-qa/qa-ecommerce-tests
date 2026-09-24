# Casos de Teste — E-commerce

## 1. Objetivo

Documentar os casos de teste elaborados para validar as principais funcionalidades da aplicação de e-commerce.

Os testes serão utilizados para verificar se o sistema apresenta o comportamento esperado diante de diferentes condições de uso.

---

## 2. Casos de Teste — Login

### CT-001 — Login com credenciais válidas

**Objetivo:**
Validar o login de um usuário utilizando credenciais válidas.

**Pré-condição:**
Usuário previamente cadastrado no sistema.

**Dados de teste:**

* E-mail: usuário válido
* Senha: senha válida

**Passos:**

1. Acessar a página de login.
2. Informar um e-mail válido.
3. Informar uma senha válida.
4. Clicar no botão "Entrar".

**Resultado esperado:**
O sistema deve autenticar o usuário e direcioná-lo para a área correspondente após o login.

**Resultado obtido:**
O sistema autenticou o usuário com sucesso e permitiu o acesso à área interna da aplicação.

**Status:**
Aprovado

**Evidência:**
Captura de tela da área interna após o login.
---

### CT-002 — Login com senha inválida

**Objetivo:**
Validar o comportamento do sistema quando o usuário informa uma senha incorreta.

**Pré-condição:**
Usuário previamente cadastrado no sistema.

**Dados de teste:**

* E-mail: usuário válido
* Senha: senha inválida

**Passos:**

1. Acessar a página de login.
2. Informar um e-mail válido.
3. Informar uma senha incorreta.
4. Clicar no botão "Entrar".

**Resultado esperado:**
O sistema não deve autenticar o usuário e deve apresentar uma mensagem informando que as credenciais são inválidas.

**Resultado obtido:**
O sistema impediu o login e apresentou uma mensagem informando que o usuário e a senha não correspondem.

**Status:**
Aprovado

**Evidência:**
Captura de tela da mensagem de erro apresentada após a tentativa de login.

---

### CT-003 — Login com usuário inválido

**Objetivo:**
Validar o comportamento do sistema quando o usuário informa um usuário inválido.

**Pré-condição:**
Acessar a página de login.

**Dados de teste:**

* Usuário: usuário inexistente
* Senha: senha válida

**Passos:**

1. Acessar a página de login.
2. Informar um usuário inexistente.
3. Informar uma senha válida.
4. Clicar no botão "Login".

**Resultado esperado:**
O sistema deve impedir o login e apresentar uma mensagem informando que as credenciais não correspondem.

**Resultado obtido:**
O sistema impediu o login e apresentou uma mensagem informando que o usuário e a senha não correspondem.

**Status:**
Aprovado

**Evidência:**
Captura de tela da mensagem de erro apresentada após a tentativa de login.

---

### CT-004 — Login com campos obrigatórios vazios

**Objetivo:**
Validar o comportamento do sistema quando os campos obrigatórios do login não são preenchidos.

**Pré-condição:**
Acessar a página de login.

**Dados de teste:**

* E-mail: vazio
* Senha: vazia

**Passos:**

1. Acessar a página de login.
2. Não preencher o campo de e-mail.
3. Não preencher o campo de senha.
4. Clicar no botão "Entrar".

**Resultado esperado:**
O sistema deve impedir o login e informar que os campos obrigatórios precisam ser preenchidos.

**Resultado obtido:**
O sistema impediu o login e apresentou a mensagem "Epic sadface: Username is required".

**Status:**
Aprovado

**Evidência:**
Captura de tela da mensagem de validação apresentada após a tentativa de login.

---

### CT-005 — Login após logout

**Objetivo:**
Validar se o usuário consegue realizar um novo login após efetuar o logout.

**Pré-condição:**
Usuário cadastrado e autenticado no sistema.

**Dados de teste:**

* E-mail: usuário válido
* Senha: senha válida

**Passos:**

1. Realizar login com credenciais válidas.
2. Acessar a opção de logout.
3. Confirmar que o usuário foi desconectado.
4. Acessar novamente a página de login.
5. Informar e-mail e senha válidos.
6. Clicar no botão "Entrar".

**Resultado esperado:**
O sistema deve permitir que o usuário realize um novo login normalmente após o logout.

**Resultado obtido:**
O sistema permitiu que o usuário realizasse um novo login normalmente após efetuar logout.

**Status:**
Aprovado

**Evidência:**
Captura de tela da área interna após o novo login.

