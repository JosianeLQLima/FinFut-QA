# Plano de Testes — FinFut

## 1. Identificação do Projeto

| Informação                   | Descrição                                |
| ---------------------------- | ---------------------------------------- |
| **Projeto**                  | FinFut                                   |
| **Tipo de projeto**          | Aplicação de controle financeiro pessoal |
| **Área**                     | Quality Assurance                        |
| **Tipo de teste principal**  | Testes Manuais                           |
| **Responsável pelos testes** | Josiane Lima                             |
| **Status**                   | Em desenvolvimento                       |
| **Versão**                   | 1.0                                      |

---

## 2. Objetivo

O objetivo deste plano de testes é definir a estratégia utilizada para validar a qualidade da aplicação FinFut.

Os testes terão como finalidade verificar se as funcionalidades estão funcionando conforme os requisitos definidos, identificar comportamentos inesperados e registrar os defeitos encontrados durante a execução.

O plano também servirá como guia para organização das atividades de QA durante o desenvolvimento do projeto.

---

## 3. Escopo dos Testes

### 3.1 Funcionalidades que serão testadas

Serão testadas as principais funcionalidades da aplicação:

* Cadastro de usuário;
* Login;
* Cadastro de receitas;
* Cadastro de despesas;
* Cadastro de contas a pagar;
* Cadastro de contas a receber;
* Categorias;
* Visualização das movimentações;
* Edição de movimentações;
* Exclusão de movimentações;
* Alteração de status;
* Resumo financeiro;
* Filtros;
* Validação dos campos;
* Isolamento dos dados dos usuários.

---

## 4. Fora do Escopo

Neste primeiro ciclo do projeto, não serão priorizados:

* Testes de carga em grande escala;
* Testes de segurança avançados;
* Testes de penetração;
* Testes de automação;
* Testes de infraestrutura;
* Testes de recuperação de desastres;
* Testes em dispositivos físicos específicos.

Esses itens poderão ser considerados futuramente caso o projeto evolua.

---

## 5. Estratégia de Testes

A estratégia será baseada principalmente em **testes manuais**, utilizando os requisitos e regras de negócio como referência.

O processo seguirá as seguintes etapas:

```text
Análise dos Requisitos
        ↓
Identificação dos Cenários
        ↓
Criação dos Casos de Teste
        ↓
Preparação dos Dados
        ↓
Execução dos Testes
        ↓
Registro dos Resultados
        ↓
Registro dos Bugs
        ↓
Correção
        ↓
Reteste
        ↓
Teste de Regressão
```

---

## 6. Tipos de Testes

### 6.1 Testes Funcionais

Verificar se cada funcionalidade apresenta o comportamento esperado de acordo com os requisitos.

---

### 6.2 Testes de Validação

Verificar o comportamento dos campos quando são utilizados:

* Dados válidos;
* Dados inválidos;
* Campos vazios;
* Caracteres especiais;
* Valores incorretos;
* Valores limites.

---

### 6.3 Testes Positivos

Validar os fluxos utilizando dados válidos e condições esperadas.

**Exemplo:**

Cadastrar uma receita utilizando descrição, valor, data e categoria válidos.

**Resultado esperado:**

A receita deve ser cadastrada corretamente.

---

### 6.4 Testes Negativos

Verificar como o sistema se comporta diante de entradas inválidas ou situações inesperadas.

**Exemplo:**

Tentar cadastrar uma despesa sem informar o valor.

**Resultado esperado:**

O sistema deve impedir o cadastro e informar o usuário sobre o campo obrigatório.

---

### 6.5 Testes de Interface

Verificar elementos visuais da aplicação, como:

* Botões;
* Campos;
* Menus;
* Tabelas;
* Mensagens;
* Formulários;
* Alinhamento;
* Textos;
* Ícones.

---

### 6.6 Testes de Usabilidade

Avaliar se a aplicação é simples e intuitiva para o usuário.

Serão observados:

* Facilidade de navegação;
* Clareza das informações;
* Organização das telas;
* Facilidade para realizar tarefas;
* Mensagens apresentadas ao usuário.

---

### 6.7 Testes de Compatibilidade

Verificar o comportamento da aplicação em diferentes navegadores.

Inicialmente serão considerados:

* Google Chrome;
* Microsoft Edge;
* Mozilla Firefox.

---

### 6.8 Testes de Regressão

Após correções de bugs, serão executados novamente testes relacionados às funcionalidades alteradas para verificar se as correções não introduziram novos problemas.

---

### 6.9 Testes Exploratórios

Serão realizados testes exploratórios para identificar comportamentos inesperados que não tenham sido previamente contemplados nos casos de teste.

---

## 7. Ambiente de Testes

Os testes serão realizados inicialmente em ambiente web.

### Ambiente previsto

| Item                   | Configuração                     |
| ---------------------- | -------------------------------- |
| Sistema operacional    | Windows                          |
| Plataforma             | Web                              |
| Navegador principal    | Google Chrome                    |
| Navegadores adicionais | Microsoft Edge / Mozilla Firefox |
| Resolução principal    | 1280 × 720                       |
| Tipo de execução       | Manual                           |

A configuração poderá ser alterada conforme a evolução da aplicação.

---

## 8. Dados de Teste

Serão utilizados dados fictícios exclusivamente para execução dos testes.

### Exemplos de dados

**Usuário:**

```text
Nome: Usuário Teste
E-mail: usuario.teste@example.com
Senha: Teste@123
```

**Receita:**

```text
Descrição: Salário
Valor: 1500,00
Categoria: Salário
```

**Despesa:**

```text
Descrição: Supermercado
Valor: 250,00
Categoria: Alimentação
```

**Conta a pagar:**

```text
Descrição: Conta de energia
Valor: 100,00
Status: Pendente
```

**Conta a receber:**

```text
Descrição: Freelance
Valor: 500,00
Status: Pendente
```

> Os dados acima são exemplos e poderão ser substituídos durante a execução dos testes.

---

## 9. Técnicas de Teste

Quando aplicável, serão utilizadas técnicas de teste para aumentar a cobertura dos cenários.

### 9.1 Particionamento de Equivalência

Os dados de entrada serão divididos em grupos válidos e inválidos.

**Exemplo:**

Para um campo que aceite valores positivos:

* Valor positivo → válido;
* Zero → verificar regra definida;
* Valor negativo → inválido;
* Campo vazio → inválido.

---

### 9.2 Análise de Valor Limite

Serão testados valores próximos aos limites definidos pelos requisitos.

**Exemplo:**

Se um campo possuir limite mínimo e máximo:

```text
Valor abaixo do mínimo
Valor mínimo
Valor dentro do limite
Valor máximo
Valor acima do máximo
```

---

### 9.3 Tabela de Decisão

Quando uma funcionalidade possuir diferentes condições e resultados, poderão ser utilizadas tabelas de decisão para identificar combinações de cenários.

---

## 10. Critérios de Entrada

Os testes poderão ser iniciados quando:

* Os requisitos estiverem disponíveis;
* A funcionalidade estiver implementada;
* O ambiente estiver acessível;
* Os dados necessários estiverem preparados;
* Os casos de teste estiverem definidos;
* A funcionalidade estiver disponível para validação.

---

## 11. Critérios de Saída

O ciclo de testes poderá ser encerrado quando:

* Os principais casos de teste forem executados;
* Os requisitos prioritários tiverem sido validados;
* Os bugs encontrados estiverem documentados;
* Os bugs críticos forem corrigidos ou avaliados;
* Os testes de regressão necessários forem realizados;
* Os resultados forem registrados.

---

## 12. Classificação de Severidade

Os bugs encontrados serão classificados de acordo com seu impacto.

| Severidade  | Descrição                                                                   |
| ----------- | --------------------------------------------------------------------------- |
| **Crítica** | Impede o funcionamento da aplicação ou causa perda grave de dados.          |
| **Alta**    | Afeta uma funcionalidade importante e impede ou dificulta seu uso.          |
| **Média**   | Afeta parcialmente uma funcionalidade, mas existe uma alternativa.          |
| **Baixa**   | Problema com baixo impacto, geralmente visual ou de pequena inconsistência. |

---

## 13. Classificação de Prioridade

| Prioridade | Descrição                                                  |
| ---------- | ---------------------------------------------------------- |
| **Alta**   | Deve ser corrigido com urgência.                           |
| **Média**  | Deve ser corrigido, mas não impede o andamento do projeto. |
| **Baixa**  | Pode ser corrigido posteriormente.                         |

---

## 14. Gerenciamento de Bugs

Os problemas encontrados durante os testes serão documentados na pasta:

```text
05-Bugs/
```

Cada bug deverá conter, quando aplicável:

* ID;
* Título;
* Data;
* Ambiente;
* Pré-condições;
* Passos para reprodução;
* Resultado esperado;
* Resultado atual;
* Severidade;
* Prioridade;
* Evidência;
* Status.

---

## 15. Evidências

As evidências dos testes serão armazenadas na pasta:

```text
06-Evidencias/
```

Poderão ser utilizadas:

* Capturas de tela;
* Vídeos curtos;
* Registros de execução;
* Evidências de API;
* Outros arquivos necessários para comprovação do resultado.

---

## 16. Ferramentas

As principais ferramentas previstas para o projeto são:

| Ferramenta        | Utilização                           |
| ----------------- | ------------------------------------ |
| **GitHub**        | Versionamento e documentação         |
| **Excel**         | Casos de teste e checklists          |
| **Google Chrome** | Testes da aplicação                  |
| **DevTools**      | Inspeção e análise da aplicação      |
| **Postman**       | Testes de API, quando aplicável      |
| **SQL**           | Validação de dados, quando aplicável |
| **Markdown**      | Documentação                         |

---

## 17. Riscos

| Risco                        | Impacto | Mitigação                                   |
| ---------------------------- | ------- | ------------------------------------------- |
| Requisitos incompletos       | Alto    | Revisar os requisitos antes dos testes      |
| Alteração de funcionalidades | Médio   | Atualizar casos de teste                    |
| Falha no ambiente            | Alto    | Verificar disponibilidade antes da execução |
| Pouco tempo para testes      | Médio   | Priorizar funcionalidades críticas          |
| Dados de teste inadequados   | Médio   | Preparar dados válidos e inválidos          |
| Correção gerar novos bugs    | Médio   | Executar testes de regressão                |

---

## 18. Cronograma

O projeto será desenvolvido de forma incremental.

| Etapa        | Atividade                                                      |
| ------------ | -------------------------------------------------------------- |
| **Semana 1** | Levantamento e documentação dos requisitos                     |
| **Semana 2** | Planejamento e criação dos casos de teste                      |
| **Semana 3** | Execução dos testes e registro dos primeiros bugs              |
| **Semana 4** | Retestes, testes de regressão e complementação da documentação |
| **Semana 5** | Consolidação dos resultados e preparação da apresentação       |

---

## 19. Entregáveis

Ao final do projeto serão produzidos os seguintes artefatos:

* Requisitos funcionais;
* Requisitos não funcionais;
* Histórias de usuário;
* Regras de negócio;
* Plano de testes;
* Casos de teste;
* Checklists;
* Relatórios de bugs;
* Evidências;
* Testes de API, quando aplicável;
* Consultas SQL, quando aplicável;
* Matriz de rastreabilidade;
* Relatório final;
* Apresentação do projeto.

---

## 20. Resultado Esperado

Espera-se que a execução do plano de testes permita identificar problemas antes da disponibilização da aplicação ao usuário final.

Além da validação do FinFut, este projeto tem como objetivo demonstrar na prática conhecimentos de **Quality Assurance**, incluindo análise de requisitos, planejamento, criação e execução de testes, identificação de bugs, documentação e acompanhamento das correções.

---

## 21. Status do Plano

**Status:** Em desenvolvimento 🚧

Este plano poderá ser atualizado conforme novas funcionalidades, requisitos ou necessidades de teste sejam identificados durante o desenvolvimento do FinFut.
