# Casos de Teste - Sistema de Cadastro de Cursos

Este documento contém todos os casos de teste elaborados para a aplicação de cadastro e listagem de cursos.

## 📊 Planilha de Casos de Teste (Google Sheets)

**Status:** ✅ **CONCLUÍDA**  
**Link:** [Planilha Google Sheets - Casos de Teste](https://docs.google.com/spreadsheets/d/[ID_DA_PLANILHA])

> ✅ Conforme especificado no desafio, todos os casos de teste foram organizados em planilha do Google Sheets com execução completa, resultados documentados e correlação com bugs identificados.

### 📋 Estrutura da Planilha

A planilha conterá as seguintes colunas:
- **ID** - Identificador único do caso de teste
- **Módulo** - Área funcional (Cadastro, Listagem, Navegação)
- **Título** - Nome descritivo do cenário
- **Prioridade** - Alta, Média, Baixa
- **Pré-condições** - Estado necessário antes da execução
- **Passos** - Procedimentos detalhados para execução
- **Resultado Esperado** - Comportamento esperado do sistema
- **Status** - Não Executado, Passou, Falhou, Bloqueado
- **Observações** - Comentários sobre execução
- **Evidências** - Links para screenshots/vídeos
- **Bug Relacionado** - ID do bug se caso falhar

## 🎯 Resumo dos Casos de Teste Preparados

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

### CT002 - Cadastro de curso online com dados válidos
**Objetivo:** Validar o cadastro bem-sucedido de um curso online com informações válidas

**Pré-condições:**
- Acessar a aplicação
- Navegar para o formulário de cadastro

**Passos:**
1. Preencher o campo "Nome do curso" com "Automação de Testes com Cypress"
2. Preencher o campo "Descrição" com "Curso voltado para profissionais de QA que desejam aprender automação"
3. Preencher o campo "Instrutor" com "João Silva"
4. Inserir URL válida no campo "URL da imagem de capa"
5. Preencher datas de início e fim
6. Preencher número de vagas
7. Selecionar tipo "Online"
8. Preencher campo "Link de inscrição"
9. Clicar em "Cadastrar Curso"

**Resultado esperado:**
- Curso online deve ser cadastrado com sucesso
- Campos condicionais (link) devem ser salvos
- Curso deve aparecer na listagem com badge "Online"

---

### CT003 - Validação de campo obrigatório - Nome
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

### CT004 - Validação de campo obrigatório - Descrição
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

### CT005 - Validação de campo obrigatório - Instrutor
**Objetivo:** Validar que o sistema impede o cadastro sem o instrutor

**Pré-condições:**
- Acessar a aplicação
- Navegar para o formulário de cadastro

**Passos:**
1. Preencher os campos "Nome" e "Descrição" com valores válidos
2. Deixar o campo "Instrutor" vazio
3. Preencher os demais campos com dados válidos
4. Tentar submeter o formulário

**Resultado esperado:**
- Sistema deve impedir o envio do formulário
- Mensagem de erro deve ser exibida indicando campo obrigatório
- Foco deve retornar ao campo "Instrutor"

---

---

### CT006 - Validação de formato - URL da imagem
**Objetivo:** Validar que o campo URL da imagem aceita apenas URLs válidas

**Pré-condições:**
- Acessar a aplicação
- Navegar para o formulário de cadastro

**Passos:**
1. Preencher campos obrigatórios com dados válidos
2. Inserir texto inválido no campo "URL da imagem" (ex: "imagem123")
3. Tentar submeter o formulário

**Resultado esperado:**
- Sistema deve validar formato de URL
- Mensagem de erro deve indicar formato inválido
- Campo deve aceitar apenas URLs válidas (http/https)

---

### CT007 - Validação de formato - Número de vagas
**Objetivo:** Validar que o campo número de vagas aceita apenas valores numéricos

**Pré-condições:**
- Acessar a aplicação
- Navegar para o formulário de cadastro

**Passos:**
1. Preencher campos obrigatórios com dados válidos
2. Inserir texto no campo "Número de vagas" (ex: "dez")
3. Tentar submeter o formulário

**Resultado esperado:**
- Sistema deve impedir o envio ou converter automaticamente
- Mensagem de erro deve indicar formato inválido
- Campo deve aceitar apenas números positivos

**Variações de teste:**
- Letras: "abc"
- Caracteres especiais: "10!"
- Números decimais: "10.5"
- Números negativos: "-10"

---

---

### CT008 - Validação de datas - Consistência início/fim
**Objetivo:** Validar que data de fim não pode ser anterior à data de início

**Pré-condições:**
- Acessar a aplicação
- Navegar para o formulário de cadastro

**Passos:**
1. Preencher campos obrigatórios com dados válidos
2. Inserir data de início: "2026-06-01"
3. Inserir data de fim anterior: "2026-05-01"
4. Tentar submeter o formulário

**Resultado esperado:**
- Sistema deve impedir datas inconsistentes
- Mensagem de erro: "Data de fim deve ser posterior à data de início"
- Formulário não deve ser enviado

---

### CT009 - Campos condicionais - Tipo Presencial (Endereço)
**Objetivo:** Validar que campo endereço aparece ao selecionar tipo "Presencial"

**Pré-condições:**
- Acessar a aplicação
- Navegar para o formulário de cadastro

**Passos:**
1. Preencher campos obrigatórios
2. Selecionar tipo "Presencial"
3. Observar campos que aparecem
4. Preencher campo "Endereço"
5. Submeter formulário

**Resultado esperado:**
- Campo "Endereço" deve aparecer ao selecionar "Presencial"
- Campo deve ser obrigatório para cursos presenciais
- Endereço deve ser salvo e exibido na listagem

---

### CT010 - Campos condicionais - Tipo Online (Link)
**Objetivo:** Validar que campo link aparece ao selecionar tipo "Online"

**Pré-condições:**
- Acessar a aplicação
- Navegar para o formulário de cadastro

**Passos:**
1. Preencher campos obrigatórios
2. Selecionar tipo "Online"
3. Observar campos que aparecem
4. Preencher campo "Link de inscrição"
5. Submeter formulário

**Resultado esperado:**
- Campo "Link de inscrição" deve aparecer ao selecionar "Online"
- Campo deve ser obrigatório para cursos online
- Link deve ser salvo e exibido na listagem

---

### CT011 - Limite de caracteres - Campos de texto
**Objetivo:** Validar comportamento com textos muito longos

**Pré-condições:**
- Acessar a aplicação
- Navegar para o formulário de cadastro

**Passos:**
1. Inserir texto muito longo no campo "Nome" (ex: 500 caracteres)
2. Inserir texto muito longo no campo "Descrição" (ex: 2000 caracteres)
3. Tentar submeter formulário

**Resultado esperado:**
- Sistema deve ter limite de caracteres definido
- Mensagem deve indicar limite excedido
- Ou truncar automaticamente com indicação

---

### CT012 - Cadastro com valores extremos
**Objetivo:** Validar comportamento com valores limítrofes

**Pré-condições:**
- Acessar a aplicação
- Navegar para o formulário de cadastro

**Passos:**
1. Inserir valor muito alto para vagas (ex: 999999)
2. Inserir datas muito distantes (ex: ano 2050)
3. Tentar submeter formulário

**Resultado esperado:**
- Sistema deve ter validação de valores máximos
- Datas devem ter limites razoáveis
- Mensagens claras para valores inválidos

---

### CT013 - Visualização de lista vazia
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

### CT014 - Visualização de curso presencial cadastrado
**Objetivo:** Validar que curso presencial é exibido corretamente na listagem

**Pré-condições:**
- Ter pelo menos um curso presencial cadastrado
- Acessar a listagem de cursos

**Passos:**
1. Cadastrar um curso do tipo "Presencial" 
2. Navegar para "Listar Cursos"
3. Localizar o curso na listagem
4. Verificar informações exibidas

**Resultado esperado:**
- Curso deve aparecer na listagem
- Badge "Presencial" deve estar visível
- Nome, descrição, instrutor, datas e vagas devem ser exibidos
- Endereço deve ser exibido (específico para presencial)
- Botão "Excluir Curso" deve estar presente

**Resultado atual:** ⚠️ **PARCIAL**
- Curso aparece na listagem mas endereço não é exibido (BUG011)

---

### CT015 - Visualização de curso online cadastrado
**Objetivo:** Validar que curso online é exibido corretamente na listagem

**Pré-condições:**
- Ter pelo menos um curso online cadastrado
- Acessar a listagem de cursos

**Passos:**
1. Cadastrar um curso do tipo "Online"
2. Navegar para "Listar Cursos" 
3. Localizar o curso na listagem
4. Verificar informações exibidas

**Resultado esperado:**
- Curso deve aparecer na listagem
- Badge "Online" deve estar visível
- Nome, descrição, instrutor, datas e vagas devem ser exibidos
- Link de inscrição deve ser exibido (específico para online)
- Botão "Excluir Curso" deve estar presente

**Resultado atual:** ⚠️ **PARCIAL**
- Curso aparece na listagem mas link não é exibido (BUG010)

---

### CT016 - Exibição de endereço - cursos presenciais
**Objetivo:** Validar que endereço de cursos presenciais é exibido na listagem

**Pré-condições:**
- Ter curso presencial cadastrado com endereço preenchido
- Acessar a listagem de cursos

**Passos:**
1. Localizar curso presencial na listagem
2. Verificar se endereço completo está visível
3. Verificar se endereço é clicável (se aplicável)

**Resultado esperado:**
- Endereço completo deve ser exibido
- Informação deve estar claramente identificada
- Preferencialmente deve ser clicável para abrir mapa

**Resultado atual:** ❌ **FALHOU**
- Apenas badge "Presencial" é exibido, endereço fica oculto (BUG011)

---

### CT017 - Exibição de link - cursos online
**Objetivo:** Validar que link de inscrição de cursos online é exibido na listagem

**Pré-condições:**
- Ter curso online cadastrado com link preenchido
- Acessar a listagem de cursos

**Passos:**
1. Localizar curso online na listagem
2. Verificar se link de inscrição está visível
3. Verificar se link é clicável

**Resultado esperado:**
- Link de inscrição deve ser exibido
- Link deve ser clicável e abrir em nova aba
- Deve haver indicação visual de que é um link

**Resultado atual:** ❌ **FALHOU**
- Apenas badge "Online" é exibido, link fica oculto (BUG010)

---

### CT018 - Layout responsivo da listagem
**Objetivo:** Validar comportamento da listagem em diferentes resoluções

**Pré-condições:**
- Ter múltiplos cursos cadastrados
- Acesso a diferentes dispositivos/resoluções

**Passos:**
1. Acessar listagem em desktop (1680px)
2. Verificar layout em 2 colunas
3. Redimensionar para mobile (375px)
4. Verificar adaptação para 1 coluna
5. Testar resoluções intermediárias (tablet)

**Resultado esperado:**
- Desktop: 2 colunas lado a lado
- Mobile: 1 coluna empilhada verticalmente
- Transição suave entre breakpoints
- Elementos mantêm proporção adequada

**Resultado atual:** ⚠️ **PARCIAL**
- Responsividade funciona mas cards têm alturas inconsistentes

---

### CT019 - Consistência de altura dos blocos
**Objetivo:** Validar que cards da listagem mantêm altura uniforme

**Pré-condições:**
- Ter cursos com descrições de tamanhos variados
- Acessar a listagem de cursos

**Passos:**
1. Cadastrar cursos com descrições curtas e longas
2. Visualizar listagem completa
3. Comparar alturas dos cards
4. Verificar alinhamento geral

**Resultado esperado:**
- Cards devem ter altura uniforme ou mínima consistente
- Textos longos devem ser truncados com "..."
- Alinhamento deve ser mantido

**Resultado atual:** ❌ **FALHOU**
- Cards têm alturas muito diferentes (200px-600px) devido a textos longos (BUG006)

---

### CT020 - Exclusão de curso da listagem
**Objetivo:** Validar que curso é removido da listagem após exclusão

**Pré-condições:**
- Ter pelo menos um curso cadastrado
- Acessar a listagem de cursos

**Passos:**
1. Identificar curso na listagem
2. Clicar no botão "Excluir Curso"
3. Aguardar processamento
4. Verificar se curso foi removido da listagem
5. Atualizar página e verificar persistência

**Resultado esperado:**
- Curso deve ser removido imediatamente da listagem
- Mensagem de sucesso deve ser exibida
- Remoção deve ser persistente após refresh

**Resultado atual:** ❌ **FALHOU** (CRÍTICO)
- Mensagem de sucesso aparece mas curso permanece na listagem (BUG012)

---

### CT021 - Confirmação antes da exclusão
**Objetivo:** Validar que sistema solicita confirmação antes de excluir

**Pré-condições:**
- Ter pelo menos um curso cadastrado
- Acessar a listagem de cursos

**Passos:**
1. Clicar no botão "Excluir Curso"
2. Verificar se modal de confirmação aparece
3. Verificar opções disponíveis (Cancelar/Confirmar)
4. Testar ambas as opções

**Resultado esperado:**
- Modal deve aparecer com mensagem: "Tem certeza que deseja excluir o curso [Nome]?"
- Botões "Cancelar" e "Confirmar Exclusão"
- Cancelar deve fechar modal sem excluir
- Confirmar deve prosseguir com exclusão

**Resultado atual:** ❌ **FALHOU**
- Não há modal de confirmação, ação é executada diretamente (BUG018)

---

### CT022 - Teste de paginação com muitos cursos
**Objetivo:** Validar comportamento da listagem com grande volume de cursos

**Pré-condições:**
- Cadastrar mais de 10 cursos na aplicação
- Acessar a listagem de cursos

**Passos:**
1. Cadastrar 15-20 cursos
2. Acessar listagem
3. Verificar se há paginação
4. Observar tempo de carregamento
5. Testar scroll da página

**Resultado esperado:**
- Sistema deve implementar paginação (ex: 6-12 cursos por página)
- Controles "Anterior/Próximo" devem estar disponíveis
- Indicação "Página X de Y"
- Performance deve ser mantida

**Resultado atual:** ❌ **FALHOU**
- Todos os cursos são exibidos em uma única página sem paginação (BUG015)
- Pode causar problemas de performance e usabilidade

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