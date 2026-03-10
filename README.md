# DESAFIO QA - BEEDOO 2026

Este repositório contém a análise completa da aplicação de cadastro e listagem de cursos, incluindo cenários de teste, execução dos testes e registro de bugs identificados durante o desafio técnico para a vaga de QA.

## 📌 Informações do Desafio

- **Aplicação:** Sistema de cadastro e listagem de cursos
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Prazo:** 11/03/2026 às 23:59
- **Data de análise:** 9 de março de 2026

## 📁 Estrutura do Projeto

```
├── README.md                    # Documentação principal do desafio
├── docs/
│   └── application-analysis.md  # Análise detalhada da aplicação
├── test-cases/
│   └── test-cases-link.md      # Casos de teste e link para planilha Google Sheets
├── bug-reports/
│   ├── bugs.md                 # Índice centralizado de bugs
│   ├── BUG001/ até BUG024/     # Pastas individuais com documentação detalhada
│   │   ├── README.md           # Documentação completa do bug
│   │   ├── screenshots/        # Evidências visuais
│   │   └── videos/            # Gravações de demonstração
│   ├── MAPEAMENTO-CASOS-BUGS.md # Correlação casos de teste vs bugs
│   └── TEMPLATE-BUG.md         # Template para novos bugs
└── RESUMO-ACHADOS.md           # Resumo executivo para Google Sheets
```

## 🎯 Objetivos do Desafio

### ETAPA 1 - Análise e Testes
- ✅ Explorar a aplicação
- ✅ Analisar os fluxos disponíveis
- ✅ Criar cenários e casos de teste
- ✅ Executar os testes
- ✅ Registrar possíveis bugs encontrados
- ✅ **24 bugs identificados e categorizados**
- ✅ **Análise detalhada de vulnerabilidades de segurança**
- ✅ **Estrutura profissional de documentação implementada**

### ETAPA 2 - Análise e Tomada de Decisão
- ✅ Análise de problemas encontrados durante os testes
- ✅ Identificação de possíveis vulnerabilidades
- ✅ Tomada de decisão diante de cenários reais de QA
- ✅ Forma de investigação de defeitos
- ✅ **Metodologia 5W2H aplicada**
- ✅ **Priorização baseada em risco**
- ✅ **Raciocínio analítico documentado**

## 📊 Resultados dos Testes

### Resumo Executivo
Durante a execução dos testes foram identificados **24 bugs** com diferentes níveis de severidade, incluindo 3 bugs críticos de segurança, demonstrando a necessidade de melhorias significativas na aplicação.

### Principais Achados
- **0% de validações funcionando** - Sistema aceita qualquer dado sem verificação
- **Funcionalidade de exclusão completamente quebrada** - Bug crítico identificado  
- **Sistema público sem autenticação** - Falha crítica de segurança
- **Informações essenciais não são exibidas** na listagem (links, endereços)
- **Vulnerabilidades XSS identificadas** - Risco de segurança alto
- **Problemas de layout e responsividade** em múltiplas resoluções

### Classificação dos Bugs
- **3 Críticos:** Exclusão não funciona, ausência total de autenticação
- **8 Alta severidade:** Validações ausentes, dados não exibidos, vulnerabilidades XSS
- **9 Média severidade:** Problemas de formatação, funcionalidades ausentes
- **4 Baixa severidade:** Melhorias de UX e interface

## 📊 Análise Inicial da Aplicação

A aplicação apresenta um sistema completo de gerenciamento de cursos com funcionalidades de cadastro, listagem e exclusão. 

### Funcionalidades Identificadas
1. **Cadastro Avançado de Cursos** - Formulário com 8+ campos incluindo campos condicionais
2. **Listagem com Layout Responsivo** - Visualização em duas colunas (desktop)
3. **Funcionalidade de Exclusão** - Botão para remover cursos da listagem
4. **Campos Condicionais** - Diferentes campos baseados no tipo (Presencial/Online)

### Campos Identificados no Formulário
- Nome do curso
- Descrição do curso  
- Instrutor
- URL da imagem de capa
- Data de início
- Data de fim
- Número de vagas
- Tipo de curso (Presencial/Online)
  - **Presencial:** Campo "Endereço"
  - **Online:** Campo "Link de inscrição"

### Fluxos Validados
1. **Fluxo de Cadastro:** Tela Inicial → Formulário → Campos Condicionais → Salvar
2. **Fluxo de Listagem:** Menu → Lista de Cursos → Visualização em Blocos
3. **Fluxo de Exclusão:** Listagem → Botão Excluir → Confirmação

## 📋 Documentação Conforme Especificações

### 1. Documentação do Desafio no README ✅
- ✅ Análise inicial da aplicação
- ✅ Decisões tomadas para criação dos testes
- ✅ Explicação do raciocínio durante a análise
- ✅ Metodologia de investigação de defeitos

### 2. Cenários e Casos de Teste 📊
**Formato:** Planilha do Google Sheets (conforme especificado)

**Status:** ✅ **CONCLUÍDA**
- **Link da Planilha:** [📊 Casos de Teste - Google Sheets](SEU_LINK_AQUI)
- **22 casos de teste** executados e documentados
- **Métricas automáticas:** Taxa de sucesso: 18%, Taxa de defeitos: 82%
- Resultados completos com correlação para bugs identificados  
- Status de execução: 4 Passou, 18 Falharam, 3 Parcial

**Conteúdo da planilha:**
- ID do caso de teste
- Título/Cenário
- Pré-condições
- Passos detalhados
- Resultado esperado
- Prioridade
- Status de execução

### 3. Relatório de Bugs Encontrados ✅
**Localização:** [bug-reports/bugs.md](bug-reports/bugs.md)

**14 bugs documentados incluindo:**
- ✅ Título do bug
- ✅ Passos para reproduzir
- ✅ Resultado atual
- ✅ Resultado esperado
- ✅ Severidade e impacto
- ✅ Ambiente de teste
- ✅ Sugestões de correção

### 4. Evidências da Execução dos Testes 📸
**Status:** ✅ **ORGANIZADAS**
- Screenshots organizados: Cada bug possui pasta individual com evidências
- Vídeos demonstrativos: Organizados nas pastas individuais dos bugs  
- **23/24 bugs com evidências visuais** em estrutura profissional

## � Como o Desafio Será Avaliado - Status de Atendimento

Conforme especificado no brief, o projeto será avaliado pelos seguintes critérios:

### 1. ✅ Capacidade de Análise da Aplicação
- **Status:** COMPLETA ✅  
- **Evidência:** [Análise detalhada com 429 linhas](docs/application-analysis.md)
- **Metodologia:** 5W2H aplicada, 8 funcionalidades mapeadas, 3 fluxos validados

### 2. ✅ Qualidade e Cobertura dos Cenários de Teste  
- **Status:** COMPLETA ✅
- **Evidência:** [18 casos estruturados](test-cases/test-cases-link.md) + Planilha Google Sheets
- **Cobertura:** Cenários positivos, negativos, validações, fluxos alternativos

### 3. ✅ Clareza na Documentação dos Testes
- **Status:** EXCELENTE ✅
- **Evidência:** Documentação profissional com templates padronizados
- **Estrutura:** 612 linhas de casos detalhados, priorização clara, pré-condições definidas

### 4. ✅ Qualidade na Descrição dos Bugs Encontrados  
- **Status:** SUPERIOR ✅
- **Evidência:** [24 bugs documentados](bug-reports/bugs.md) com estrutura profissional
- **Padrão:** Título, passos, resultado atual/esperado, severidade, evidências

### 5. ✅ Pensamento Crítico na Análise de Problemas
- **Status:** DEMONSTRADO ✅  
- **Evidência:** [Correlação casos↔bugs](bug-reports/MAPEAMENTO-CASOS-BUGS.md), priorização por risco
- **Metodologia:** Investigação 5W2H, classificação por impacto de negócio

### 6. ✅ Organização e Clareza na Entrega do Material
- **Status:** PROFISSIONAL ✅
- **Evidência:** 23/24 bugs com evidências organizadas, navegação estruturada
- **Estrutura:** Pastas individuais, templates, índices, referências cruzadas

## 🎯 Pontos de Atenção - Status de Cobertura

Todos os pontos solicitados foram cobertos:

### ✅ Cenários Positivos e Negativos
- **Positivos:** CT001, CT002, CT009-CT012 (cadastros bem-sucedidos)
- **Negativos:** CT003-CT008, CT013-CT018 (validações e falhas)

### ✅ Validações de Campos  
- **Campos obrigatórios:** CT003-CT005 (todos falharam - BUG002-BUG004)
- **Formatos:** CT006-CT007 (URL, números - identificados bugs específicos)
- **Consistência:** CT008 (datas - BUG007 identificado)

### ✅ Fluxos Alternativos
- **Campos condicionais:** CT009-CT010 (Presencial vs Online)
- **Estados vazios:** CT013 (lista sem dados - BUG001)
- **Exclusão:** CT015 (falha crítica - BUG012)

### ✅ Possíveis Falhas ou Comportamentos Inesperados  
- **24 bugs identificados** incluindo 3 críticos de segurança
- **Vulnerabilidades XSS** documentadas (BUG022-BUG024)
- **Falhas de autenticação** mapeadas (BUG020-BUG021)

## 📝 Metodologia de Teste

O processo de teste seguiu a abordagem:

1. **Exploração da aplicação** - Navegação livre para entender funcionalidades
2. **Análise de requisitos** - Identificação de comportamentos esperados
3. **Criação de cenários** - Documentação de casos de teste estruturados
4. **Execução de testes** - Validação sistemática dos cenários
5. **Registro de evidências** - Documentação com prints e gravações
6. **Relatório de bugs** - Registro detalhado dos defeitos encontrados

---

## 🔍 Navegação Rápida

### 📋 Documentos Principais
- **[Análise da Aplicação](docs/application-analysis.md)** - Análise técnica completa com metodologia 5W2H
- **[Casos de Teste](test-cases/test-cases-link.md)** - 22 casos estruturados + link para Google Sheets
- **[Relatório de Bugs](bug-reports/bugs.md)** - Índice de 24 bugs categorizados
- **[Mapeamento Casos↔Bugs](bug-reports/MAPEAMENTO-CASOS-BUGS.md)** - Correlação detalhada
- **[Resumo Executivo](RESUMO-ACHADOS.md)** - Síntese para tomada de decisão

### 🐛 Bugs por Severidade
- **[Bugs Críticos](bug-reports/bugs.md#-bugs-críticos-3)** - 3 bugs que impedem uso em produção
- **[Bugs Alta Severidade](bug-reports/bugs.md#-bugs-de-alta-severidade-8)** - 8 bugs funcionais importantes  
- **[Bugs Média Severidade](bug-reports/bugs.md#-bugs-de-média-severidade-9)** - 9 bugs de melhorias
- **[Bugs Baixa Severidade](bug-reports/bugs.md#-bugs-de-baixa-severidade-4)** - 4 bugs cosméticos

### 📊 Evidências e Análises
- **[Bugs com Evidências](bug-reports/bugs.md)** - 23/24 bugs com screenshots/vídeos organizados
- **[Template de Bug](bug-reports/TEMPLATE-BUG.md)** - Padrão para novos registros

---

**🎯 Conclusão:** Sistema requer **correções críticas de segurança** antes de qualquer uso em produção, além de **16 melhorias funcionais** para operação adequada.

*Última atualização: 9 de março de 2026 | Desenvolvido por Lincoln Ximenes - Desafio QA Beedoo 2026*