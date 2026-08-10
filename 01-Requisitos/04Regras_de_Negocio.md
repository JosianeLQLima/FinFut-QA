# Regras de Negócio — FinFut

## 1. Objetivo

As regras de negócio definem as condições que devem ser respeitadas pela aplicação FinFut durante o funcionamento de suas principais funcionalidades.

Essas regras serão utilizadas como referência para elaboração e execução dos testes.

---

## RN-001 — Cadastro de usuário

Cada conta deve possuir um e-mail único.

Não deve ser permitido cadastrar dois usuários utilizando o mesmo e-mail.

---

## RN-002 — Autenticação

Somente usuários cadastrados com credenciais válidas poderão acessar suas informações financeiras.

---

## RN-003 — Campos obrigatórios

Os campos definidos como obrigatórios devem ser preenchidos antes que o formulário possa ser enviado.

---

## RN-004 — Valor financeiro

Os valores de receitas, despesas e contas devem ser maiores que zero.

Não devem ser aceitos valores negativos.

---

## RN-005 — Tipo de movimentação

Toda movimentação financeira deve possuir um tipo.

Os tipos principais são:

* Receita;
* Despesa.

---

## RN-006 — Categoria

Toda receita ou despesa deve estar associada a uma categoria.

---

## RN-007 — Conta a pagar

Uma conta a pagar deve possuir uma data de vencimento.

---

## RN-008 — Conta a receber

Uma conta a receber deve possuir uma data prevista para recebimento.

---

## RN-009 — Status da conta

As contas devem possuir um status que represente sua situação atual.

Status previstos:

* Pendente;
* Pago;
* Recebido;
* Vencido.

---

## RN-010 — Atualização do status

Quando uma conta for paga, seu status deverá ser alterado para **Pago**.

Quando uma conta for recebida, seu status deverá ser alterado para **Recebido**.

---

## RN-011 — Contas vencidas

Uma conta que ultrapassar sua data de vencimento sem ter sido paga poderá ser identificada como **Vencida**.

---

## RN-012 — Exclusão

Uma movimentação somente deverá ser excluída após a confirmação do usuário.

---

## RN-013 — Saldo

O saldo financeiro deverá ser calculado considerando as receitas e despesas registradas.

**Fórmula básica:**

```text
Saldo = Total de Receitas - Total de Despesas
```

---

## RN-014 — Dados por usuário

As movimentações financeiras devem estar associadas ao usuário responsável pelo cadastro.

Um usuário não deve visualizar ou alterar dados pertencentes a outro usuário.

---

## RN-015 — Integridade das informações

Ao editar uma movimentação, o sistema deve manter a integridade dos demais dados relacionados ao lançamento.

---

## RN-016 — Exclusão de usuário

Caso a aplicação implemente exclusão de conta, deverá existir um processo definido para tratamento dos dados financeiros associados ao usuário.

---

## RN-017 — Datas

As datas das movimentações devem ser armazenadas e apresentadas de forma consistente.

---

## RN-018 — Categorias

As categorias devem possuir nomes claros e não devem permitir duplicações desnecessárias.

---

## RN-019 — Mensagens

As mensagens apresentadas ao usuário devem informar claramente se uma operação foi realizada com sucesso ou se ocorreu algum problema.

---

## RN-020 — Rastreabilidade

Cada requisito e regra de negócio deverá estar relacionado aos respectivos casos de teste na matriz de rastreabilidade.

---

## Observação

Estas regras representam a versão inicial do projeto FinFut e poderão ser atualizadas durante o desenvolvimento da aplicação.

Alterações realizadas posteriormente deverão ser refletidas nos requisitos, casos de teste e demais documentos relacionados.
