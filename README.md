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
│   └── test-cases-link.md      # Link para planilha com casos de teste
├── bug-reports/
│   └── bugs.md                 # Relatório de bugs encontrados
└── evidences/
    ├── screenshots/            # Capturas de tela dos testes
    └── videos/                # Gravações da execução dos testes
```

## 🎯 Objetivos do Desafio

### ETAPA 1 - Análise e Testes
- ✅ Explorar a aplicação
- ✅ Analisar os fluxos disponíveis
- ✅ Criar cenários e casos de teste
- ✅ Executar os testes
- ✅ Registrar possíveis bugs encontrados

### ETAPA 2 - Análise e Tomada de Decisão
- 🔄 Análise de problemas encontrados durante os testes
- 🔄 Identificação de possíveis vulnerabilidades
- 🔄 Tomada de decisão diante de cenários reais de QA
- 🔄 Forma de investigação de defeitos

## 📊 Resultados dos Testes

### Resumo Executivo
Durante a execução dos testes foram identificados **12 bugs** com diferentes níveis de severidade, demonstrando a necessidade de melhorias significativas na aplicação.

### Principais Achados
- **0% de validações funcionando** - Sistema aceita qualquer dado
- **Funcionalidade de exclusão quebrada** - Bug crítico identificado  
- **Informações essenciais não são exibidas** na listagem
- **Problemas de layout e responsividade**

### Classificação dos Bugs
- **1 Crítico:** Funcionalidade de exclusão não funciona
- **6 Alta severidade:** Validações ausentes e dados não exibidos
- **4 Média severidade:** Problemas de formatação e layout
- **1 Baixa severidade:** Melhorias de UX

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

## 📋 Critérios de Avaliação

Durante a análise, foram considerados os seguintes aspectos:

- **Cenários positivos e negativos**
- **Validações de campos**
- **Fluxos alternativos**
- **Possíveis falhas ou comportamentos inesperados**

## 📝 Metodologia de Teste

O processo de teste seguiu a abordagem:

1. **Exploração da aplicação** - Navegação livre para entender funcionalidades
2. **Análise de requisitos** - Identificação de comportamentos esperados
3. **Criação de cenários** - Documentação de casos de teste estruturados
4. **Execução de testes** - Validação sistemática dos cenários
5. **Registro de evidências** - Documentação com prints e gravações
6. **Relatório de bugs** - Registro detalhado dos defeitos encontrados

---

## 🔍 Links Rápidos

- [📑 Análise Detalhada da Aplicação](docs/application-analysis.md)
- [🧪 Casos de Teste](test-cases/test-cases-link.md)
- [🐛 Relatório de Bugs](bug-reports/bugs.md)
- [📸 Evidências - Screenshots](evidences/screenshots/)
- [🎥 Evidências - Vídeos](evidences/videos/)

---

*Desenvolvido por Lincoln Ximenes como parte do desafio técnico para QA Júnior - Beedoo 2026*