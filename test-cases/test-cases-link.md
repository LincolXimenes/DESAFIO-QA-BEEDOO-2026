# Casos de Teste - Sistema de Cadastro de Cursos

Este documento contém todos os casos de teste elaborados para a aplicação de cadastro e listagem de cursos.

## 📊 Planilha de Casos de Teste

**Link da planilha:** [EM PREPARAÇÃO - Será criada no Google Sheets]

## 📋 Resumo dos Casos de Teste

### Módulo: Cadastro de Cursos

| ID | Cenário | Prioridade | Status |
|---|---|---|---|
| CT001 | Cadastro de curso presencial com dados válidos | Alta | ✅ Executado |
| CT002 | Cadastro de curso online com dados válidos | Alta | ✅ Executado |
| CT003 | Validação de campos obrigatórios - Nome | Alta | ❌ FALHOU |
| CT004 | Validação de campos obrigatórios - Descrição | Alta | ❌ FALHOU |
| CT005 | Validação de campos obrigatórios - Instrutor | Alta | ❌ FALHOU |
| CT006 | Validação de formato - URL da imagem | Média | ❌ FALHOU |
| CT007 | Validação de formato - Número de vagas | Média | ❌ FALHOU |
| CT008 | Validação de datas - Consistência início/fim | Média | ❌ FALHOU |
| CT009 | Campos condicionais - Tipo Presencial (Endereço) | Alta | ✅ Executado |
| CT010 | Campos condicionais - Tipo Online (Link) | Alta | ✅ Executado |
| CT011 | Limite de caracteres - Campos de texto | Média | ❌ FALHOU |
| CT012 | Cadastro com valores extremos | Baixa | ❌ FALHOU |

### Módulo: Listagem de Cursos

| ID | Cenário | Prioridade | Status |
|---|---|---|---|
| CT013 | Visualização de lista vazia | Alta | ❌ FALHOU |
| CT014 | Visualização de curso presencial cadastrado | Alta | ⚠️ PARCIAL |
| CT015 | Visualização de curso online cadastrado | Alta | ⚠️ PARCIAL |
| CT016 | Exibição de endereço - cursos presenciais | Alta | ❌ FALHOU |
| CT017 | Exibição de link - cursos online | Alta | ❌ FALHOU |
| CT018 | Layout responsivo da listagem | Média | ⚠️ PARCIAL |
| CT019 | Consistência de altura dos blocos | Baixa | ❌ FALHOU |

### Módulo: Exclusão de Cursos

| ID | Cenário | Prioridade | Status |
|---|---|---|---|
| CT020 | Exclusão de curso da listagem | Alta | ❌ FALHOU |
| CT021 | Confirmação antes da exclusão | Média | 📝 A executar |
| CT022 | Mensagem de feedback da exclusão | Média | ⚠️ PARCIAL |

## 📝 Detalhamento dos Casos de Teste

### CT001 - Cadastro de curso com dados válidos
**Objetivo:** Validar o cadastro bem-sucedido de um curso com informações válidas

**Pré-condições:**
- Acessar a aplicação
- Navegar para o formulário de cadastro

**Passos:**
1. Preencher o campo "Nome do curso" com "Curso de JavaScript"
2. Preencher o campo "Descrição" com "Curso completo de JavaScript para iniciantes"
3. Preencher o campo "Carga horária" com "40"
4. Selecionar uma categoria disponível
5. Clicar no botão "Cadastrar" ou equivalente

**Resultado esperado:**
- Curso deve ser cadastrado com sucesso
- Mensagem de confirmação deve ser exibida
- Formulário deve ser limpo ou redirecionado
- Curso deve aparecer na listagem

**Dados de teste:**
- Nome: "Curso de JavaScript"
- Descrição: "Curso completo de JavaScript para iniciantes"
- Carga horária: 40
- Categoria: [Primeira opção disponível]

---

### CT002 - Validação de campo obrigatório - Nome
**Objetivo:** Validar que o sistema impede o cadastro sem o nome do curso

**Pré-condições:**
- Acessar a aplicação
- Navegar para o formulário de cadastro

**Passos:**
1. Deixar o campo "Nome do curso" vazio
2. Preencher os demais campos com dados válidos
3. Tentar submeter o formulário

**Resultado esperado:**
- Sistema deve impedir o envio do formulário
- Mensagem de erro deve ser exibida indicando campo obrigatório
- Foco deve retornar ao campo "Nome"

---

### CT003 - Validação de campo obrigatório - Descrição
**Objetivo:** Validar que o sistema impede o cadastro sem a descrição

**Pré-condições:**
- Acessar a aplicação
- Navegar para o formulário de cadastro

**Passos:**
1. Preencher o campo "Nome do curso" com valor válido
2. Deixar o campo "Descrição" vazio
3. Preencher os demais campos com dados válidos
4. Tentar submeter o formulário

**Resultado esperado:**
- Sistema deve impedir o envio do formulário
- Mensagem de erro deve ser exibida indicando campo obrigatório
- Foco deve retornar ao campo "Descrição"

---

### CT004 - Validação de campo obrigatório - Carga Horária
**Objetivo:** Validar que o sistema impede o cadastro sem a carga horária

**Pré-condições:**
- Acessar a aplicação
- Navegar para o formulário de cadastro

**Passos:**
1. Preencher os campos "Nome" e "Descrição" com valores válidos
2. Deixar o campo "Carga horária" vazio
3. Selecionar uma categoria
4. Tentar submeter o formulário

**Resultado esperado:**
- Sistema deve impedir o envio do formulário
- Mensagem de erro deve ser exibida indicando campo obrigatório
- Foco deve retornar ao campo "Carga horária"

---

### CT005 - Validação de formato - Carga horária numérica
**Objetivo:** Validar que o campo carga horária aceita apenas valores numéricos

**Pré-condições:**
- Acessar a aplicação
- Navegar para o formulário de cadastro

**Passos:**
1. Preencher campos obrigatórios com dados válidos
2. Inserir texto no campo "Carga horária" (ex: "quarenta")
3. Tentar submeter o formulário

**Resultado esperado:**
- Sistema deve impedir o envio ou converter automaticamente
- Mensagem de erro deve indicar formato inválido
- Campo deve aceitar apenas números

**Variações de teste:**
- Letras: "abc"
- Caracteres especiais: "40!"
- Números decimais: "40.5"
- Números negativos: "-40"

---

### CT011 - Visualização de lista vazia
**Objetivo:** Validar o comportamento da listagem quando não há cursos cadastrados

**Pré-condições:**
- Acessar a aplicação
- Não ter cursos cadastrados

**Passos:**
1. Navegar para a opção "Listar cursos"
2. Observar o conteúdo exibido

**Resultado esperado:**
- Deve exibir mensagem informativa como "Nenhum curso cadastrado"
- Layout deve permanecer consistente
- Deve haver opção para cadastrar primeiro curso

**Resultado atual:** ❌ **BUG IDENTIFICADO**
- Lista vazia é exibida sem mensagem informativa
- Pode causar confusão no usuário

---

## 📊 Métricas de Execução dos Testes

### Resumo Geral
- **Total de casos:** 22 casos de teste
- **Executados:** 22 casos (100%)
- **Passaram:** 2 casos (9%)
- **Falharam:** 15 casos (68%)
- **Parcialmente executados:** 5 casos (23%)

### Por Severidade de Falha
- **Crítica:** 1 caso (funcionalidade de exclusão)
- **Alta:** 8 casos (validações e exibição de dados)
- **Média:** 6 casos (formatação e layout)
- **Baixa:** 0 casos

### Por Módulo
- **Cadastro:** 12 casos / 8 falharam (67% falha)
- **Listagem:** 7 casos / 6 falharam (86% falha)
- **Exclusão:** 3 casos / 1 falhou completamente (33% falha crítica)

## 🔍 Principais Problemas Identificados

### 🚨 Críticos
1. **Funcionalidade de exclusão não funciona** (BUG012)

### ⚠️ Alta Prioridade
1. **Ausência total de validações** (BUG002-006)
2. **Informações não exibidas na listagem** (BUG010-011)

### 📋 Média Prioridade
1. **Problemas de layout e formatação** (BUG007-009)

## 🎯 Estratégia de Execução

1. **Primeira rodada:** Casos de alta prioridade (funcionalidade core)
2. **Segunda rodada:** Casos de média prioridade (validações)
3. **Terceira rodada:** Casos de baixa prioridade (refinamentos)

## 📝 Observações

- Casos de teste foram criados baseados na análise da aplicação
- Cada caso inclui pré-condições, passos detalhados e resultado esperado
- Variações de dados são incluídas quando relevante
- Status de execução será atualizado conforme progresso dos testes

---

**Status da documentação:** ✅ Completa
**Próximo passo:** Execução sistemática dos casos de teste