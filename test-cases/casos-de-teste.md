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


---

## 3. Casos de Teste — Produtos

### CT-006 — Visualização de produtos

**Objetivo:**
Verificar se os produtos são exibidos corretamente na página inicial do e-commerce.

**Pré-condição:**
Usuário autenticado no sistema com credenciais válidas.

**Dados de teste:**
- Usuário: `standard_user`
- Senha: `secret_sauce`

**Passos:**
1. Acessar o site https://www.saucedemo.com/.
2. Informar usuário e senha válidos.
3. Clicar no botão "Login".
4. Verificar se a lista de produtos é exibida.
5. Conferir nomes, imagens, preços e botões "Add to cart".
6. Rolar a página para visualizar os demais produtos.

**Resultado esperado:**
A página deve exibir os produtos com nomes, imagens, preços e botões "Add to cart" corretamente.

**Resultado obtido:**
A página abriu corretamente e os produtos foram exibidos com nomes, imagens, preços e botões "Add to cart". Não foram identificados problemas na verificação realizada.

**Status:**
Aprovado

**Evidência:**
Captura de tela da área interna após o novo login.



## 3. Casos de Teste — Produtos



**Objetivo:**
Verificar se os produtos são exibidos corretamente na página inicial do e-commerce.

**Pré-condição:**
Usuário autenticado no sistema com credenciais válidas.

**Dados de teste:**
- Usuário: `standard_user`
- Senha: `secret_sauce`

**Passos:**
1. Acessar o site https://www.saucedemo.com/.
2. Informar usuário e senha válidos.
3. Clicar no botão "Login".
4. Verificar se a lista de produtos é exibida.
5. Conferir nomes, imagens, preços e botões "Add to cart".
6. Rolar a página para visualizar os demais produtos.

**Resultado esperado:**
A página deve exibir os produtos com nomes, imagens, preços e botões "Add to cart" corretamente.

**Resultado obtido:**
A página abriu corretamente e os produtos foram exibidos com nomes, imagens, preços e botões "Add to cart". Não foram identificados problemas na verificação realizada.

**Status:**
Aprovado

**Evidência:**
`evidences/CT-006-visualizacao-produtos.jpeg`

---

## 4. Casos de Teste — Carrinho

### CT-007 — Adicionar produto ao carrinho

**Objetivo:**

Verificar se é possível adicionar um produto ao carrinho e se a interface é atualizada corretamente.

**Pré-condição:**

Usuário autenticado no SauceDemo com credenciais válidas.

**Dados de teste:**
- Usuário: `standard_user`
- Senha: `secret_sauce`
- Produto: `Sauce Labs Backpack`

**Passos:**
1. Acessar https://www.saucedemo.com/.
2. Informar usuário e senha válidos.
3. Clicar em "Login".
4. Localizar o produto "Sauce Labs Backpack".
5. Clicar em "Add to cart".
6. Verificar se o botão muda para "Remove".
7. Verificar se o ícone do carrinho exibe a quantidade 1.

**Resultado esperado:**

O produto deve ser adicionado ao carrinho, o botão deve mudar para "Remove" e o ícone do carrinho deve indicar 1 item.

**Resultado obtido:**

O produto Sauce Labs Backpack foi adicionado corretamente. O botão mudou para "Remove" e o ícone do carrinho exibiu 1.

**Status:**

Aprovado

**Evidência:**

`evidences/CT-007-adicionar-produto-carrinho.jpeg`

---

### CT-008 — Remover produto do carrinho

**Objetivo:**

Verificar se o usuário consegue remover um produto do carrinho de compras.

**Pré-condição:**

Usuário autenticado no SauceDemo com credenciais válidas e produto adicionado ao carrinho.

**Dados de teste:**
- Usuário: `standard_user`
- Senha: `secret_sauce`
- Produto: `Sauce Labs Backpack`

**Passos:**
1. Acessar https://www.saucedemo.com/.
2. Informar usuário e senha válidos.
3. Clicar em "Login".
4. Adicionar o produto "Sauce Labs Backpack" ao carrinho.
5. Clicar no ícone do carrinho.
6. Verificar se o produto aparece na lista.
7. Clicar em "Remove".
8. Verificar se o produto desapareceu da lista e se o carrinho ficou vazio.

**Resultado esperado:**

O produto deve ser removido do carrinho e não deve mais aparecer na lista de itens.

**Resultado obtido:**

O produto foi removido corretamente. Ele desapareceu da lista e o carrinho ficou vazio.

**Status:**

Aprovado

**Evidência:**

`evidences/CT-008-remover-produto-carrinho.jpeg`

---

### CT-009 — Adicionar dois produtos ao carrinho

**Objetivo:**

Verificar se o sistema permite adicionar dois produtos diferentes ao carrinho e se a quantidade de itens é atualizada corretamente.

**Pré-condição:**

Usuário autenticado no SauceDemo com credenciais válidas.

**Dados de teste:**
- Usuário: `standard_user`
- Senha: `secret_sauce`
- Produto 1: `Sauce Labs Backpack`
- Produto 2: `Sauce Labs Bike Light`

**Passos:**
1. Acessar https://www.saucedemo.com/.
2. Informar usuário e senha válidos.
3. Clicar em "Login".
4. Localizar o produto "Sauce Labs Backpack" e clicar em "Add to cart".
5. Localizar o produto "Sauce Labs Bike Light" e clicar em "Add to cart".
6. Verificar se os dois botões mudaram para "Remove".
7. Verificar se o ícone do carrinho exibe a quantidade 2.

**Resultado esperado:**

Os dois produtos devem ser adicionados ao carrinho, os botões devem mudar para "Remove" e o ícone do carrinho deve indicar 2 itens.

**Resultado obtido:**

Os dois produtos foram adicionados corretamente. Os botões mudaram para "Remove" e o ícone do carrinho exibiu 2 itens.

**Status:**

Aprovado

**Evidência:**

`evidences/CT-009-adicionar-dois-produtos-carrinho.jpeg`
