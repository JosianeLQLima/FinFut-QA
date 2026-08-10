# Requisitos Funcionais — FinFut

## 1. Introdução

Os requisitos funcionais descrevem as funcionalidades que o sistema FinFut deverá disponibilizar ao usuário.

O objetivo desta documentação é definir de forma clara o comportamento esperado da aplicação e servir como base para a criação dos casos de teste.

---

## 2. Identificação dos Requisitos

### RF-001 — Cadastro de usuário

O sistema deve permitir que o usuário crie uma conta informando seus dados pessoais.

**Dados mínimos:**

* Nome;
* E-mail;
* Senha.

---

### RF-002 — Login

O sistema deve permitir que o usuário acesse sua conta utilizando e-mail e senha cadastrados.

**Resultado esperado:**

* Dados válidos devem permitir o acesso;
* Dados inválidos devem impedir o acesso;
* O sistema deve apresentar uma mensagem informativa em caso de erro.

---

### RF-003 — Cadastro de receita

O sistema deve permitir o cadastro de receitas financeiras.

O usuário deverá informar:

* Descrição;
* Valor;
* Data;
* Categoria;
* Observação, quando necessário.

---

### RF-004 — Cadastro de despesa

O sistema deve permitir o cadastro de despesas financeiras.

O usuário deverá informar:

* Descrição;
* Valor;
* Data;
* Categoria;
* Observação, quando necessário.

---

### RF-005 — Cadastro de conta a pagar

O sistema deve permitir cadastrar contas que deverão ser pagas.

O cadastro deverá conter:

* Descrição da conta;
* Valor;
* Data de vencimento;
* Categoria;
* Status da conta.

---

### RF-006 — Cadastro de conta a receber

O sistema deve permitir cadastrar valores que o usuário deverá receber.

O cadastro deverá conter:

* Descrição;
* Valor;
* Data prevista para recebimento;
* Categoria;
* Status.

---

### RF-007 — Categorias de receitas

O sistema deve permitir classificar receitas por categorias.

Exemplos:

* Salário;
* Freelance;
* Investimentos;
* Outros.

---

### RF-008 — Categorias de despesas

O sistema deve permitir classificar despesas por categorias.

Exemplos:

* Alimentação;
* Moradia;
* Transporte;
* Saúde;
* Educação;
* Lazer;
* Compras;
* Outros.

---

### RF-009 — Visualização das movimentações

O sistema deve permitir que o usuário visualize suas movimentações financeiras cadastradas.

A listagem deverá apresentar informações como:

* Descrição;
* Tipo;
* Valor;
* Categoria;
* Data;
* Status.

---

### RF-010 — Edição de movimentação

O sistema deve permitir que o usuário altere informações de uma receita, despesa ou conta cadastrada.

---

### RF-011 — Exclusão de movimentação

O sistema deve permitir que o usuário exclua uma movimentação cadastrada.

Antes da exclusão, o sistema deverá solicitar confirmação.

---

### RF-012 — Alteração de status

O sistema deve permitir alterar o status das contas.

Exemplos:

* Pendente;
* Pago;
* Recebido;
* Vencido.

---

### RF-013 — Resumo financeiro

O sistema deve apresentar um resumo das informações financeiras do usuário.

O resumo deverá permitir visualizar:

* Total de receitas;
* Total de despesas;
* Total a pagar;
* Total a receber;
* Saldo disponível.

---

### RF-014 — Filtro de movimentações

O sistema deve permitir filtrar movimentações por informações como:

* Período;
* Tipo;
* Categoria;
* Status.

---

### RF-015 — Validação dos dados

O sistema deve validar os dados informados nos formulários.

Campos obrigatórios não poderão ser enviados vazios e valores inválidos deverão ser rejeitados.

---

### RF-016 — Isolamento dos dados

O sistema deve garantir que cada usuário visualize apenas suas próprias informações financeiras.

---

## 3. Prioridade dos Requisitos

| Prioridade | Requisitos                                             |
| ---------- | ------------------------------------------------------ |
| Alta       | RF-001, RF-002, RF-003, RF-004, RF-005, RF-006, RF-009 |
| Média      | RF-007, RF-008, RF-010, RF-011, RF-012, RF-013         |
| Baixa      | RF-014, RF-015, RF-016                                 |

---

## 4. Observação

Os requisitos poderão ser ajustados durante o desenvolvimento da aplicação. Qualquer alteração deverá ser registrada na documentação do projeto para manter a rastreabilidade entre requisitos e testes.
