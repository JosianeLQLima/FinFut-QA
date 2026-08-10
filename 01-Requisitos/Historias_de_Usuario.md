# Histórias de Usuário — FinFut

## 1. Introdução

As histórias de usuário representam as principais necessidades do usuário dentro da aplicação FinFut.

Elas serão utilizadas como apoio para definição dos requisitos e criação dos casos de teste.

---

## HU-001 — Criar conta

**Como** novo usuário,

**Quero** criar uma conta no FinFut,

**Para** poder utilizar a aplicação e controlar minhas finanças.

### Critérios de aceitação

* O usuário deve informar nome, e-mail e senha;
* Os campos obrigatórios devem ser preenchidos;
* O e-mail deve possuir formato válido;
* O sistema deve informar quando o cadastro for realizado com sucesso;
* O sistema não deve permitir cadastro com dados inválidos.

---

## HU-002 — Acessar minha conta

**Como** usuário cadastrado,

**Quero** realizar login,

**Para** acessar minhas informações financeiras.

### Critérios de aceitação

* O usuário deve informar e-mail e senha;
* Dados válidos devem permitir o acesso;
* Dados inválidos devem impedir o acesso;
* O sistema deve apresentar mensagem de erro quando necessário.

---

## HU-003 — Cadastrar receita

**Como** usuário,

**Quero** cadastrar minhas receitas,

**Para** acompanhar quanto dinheiro recebo.

### Critérios de aceitação

* Informar descrição;
* Informar valor;
* Informar data;
* Selecionar categoria;
* Salvar a receita;
* Visualizar a receita cadastrada.

---

## HU-004 — Cadastrar despesa

**Como** usuário,

**Quero** cadastrar minhas despesas,

**Para** acompanhar meus gastos.

### Critérios de aceitação

* Informar descrição;
* Informar valor;
* Informar data;
* Selecionar categoria;
* Salvar a despesa;
* Visualizar a despesa cadastrada.

---

## HU-005 — Controlar contas a pagar

**Como** usuário,

**Quero** cadastrar minhas contas a pagar,

**Para** controlar meus compromissos financeiros.

### Critérios de aceitação

* Informar descrição;
* Informar valor;
* Informar vencimento;
* Selecionar categoria;
* Informar o status;
* Visualizar a conta cadastrada.

---

## HU-006 — Controlar contas a receber

**Como** usuário,

**Quero** cadastrar valores que tenho a receber,

**Para** acompanhar meus recebimentos futuros.

### Critérios de aceitação

* Informar descrição;
* Informar valor;
* Informar data prevista;
* Selecionar categoria;
* Informar o status;
* Visualizar o lançamento cadastrado.

---

## HU-007 — Consultar movimentações

**Como** usuário,

**Quero** visualizar minhas movimentações financeiras,

**Para** acompanhar minhas receitas e despesas.

### Critérios de aceitação

* Exibir as movimentações cadastradas;
* Apresentar descrição;
* Apresentar valor;
* Apresentar data;
* Apresentar categoria;
* Apresentar status.

---

## HU-008 — Editar movimentação

**Como** usuário,

**Quero** editar uma movimentação,

**Para** corrigir ou atualizar informações.

### Critérios de aceitação

* Permitir selecionar uma movimentação;
* Permitir alterar seus dados;
* Salvar as alterações;
* Apresentar os dados atualizados.

---

## HU-009 — Excluir movimentação

**Como** usuário,

**Quero** excluir uma movimentação,

**Para** remover informações cadastradas incorretamente.

### Critérios de aceitação

* Permitir selecionar uma movimentação;
* Solicitar confirmação;
* Excluir a movimentação após confirmação;
* Manter a movimentação caso o usuário cancele a operação.

---

## HU-010 — Visualizar resumo financeiro

**Como** usuário,

**Quero** visualizar um resumo das minhas finanças,

**Para** entender minha situação financeira.

### Critérios de aceitação

O sistema deve apresentar informações como:

* Total de receitas;
* Total de despesas;
* Total a pagar;
* Total a receber;
* Saldo.

---

## HU-011 — Filtrar movimentações

**Como** usuário,

**Quero** filtrar minhas movimentações,

**Para** encontrar informações específicas com mais facilidade.

### Critérios de aceitação

O sistema deve permitir filtros por:

* Período;
* Tipo;
* Categoria;
* Status.

---

## HU-012 — Visualizar somente meus dados

**Como** usuário,

**Quero** acessar somente minhas informações financeiras,

**Para** manter meus dados protegidos.

### Critérios de aceitação

* O usuário deve visualizar somente seus próprios lançamentos;
* Dados de outros usuários não devem ser exibidos;
* O acesso deve respeitar a autenticação da conta.
