# Análise Detalhada da Aplicação

Este documento contém a análise completa da aplicação de cadastro e listagem de cursos, incluindo funcionalidades, fluxos, requisitos identificados e pontos críticos para teste.

## 📌 Informações Gerais

- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Tipo:** Sistema web de gerenciamento de cursos
- **Tecnologia:** Aplicação web responsiva
- **Data da análise:** 9 de março de 2026

## 🎯 Objetivo da Aplicação

A aplicação tem como objetivo permitir o cadastro e gerenciamento de cursos de forma simples e intuitiva, oferecendo:

- Cadastro de novos cursos com informações básicas
- Listagem dos cursos cadastrados
- Interface amigável e responsiva

## 🔄 Principais Fluxos Identificados

### 1. Fluxo de Cadastro de Curso

**Caminho:** Tela Inicial → Cadastrar Curso → Preencher Formulário → Salvar

**Campos do formulário:**
- **Nome do curso**
- **Descrição do curso** 
- **Instrutor**
- **URL da imagem de capa**
- **Data de início**
- **Data de fim**
- **Número de vagas**
- **Tipo de curso** (Presencial/Online)
  - **Presencial:** Campo adicional "Endereço"
  - **Online:** Campo adicional "Link de inscrição"

**Comportamentos esperados:**
- Validação de campos obrigatórios
- Validação de formatos (datas, URLs, números)
- Campos condicionais baseados no tipo de curso
- Feedback de sucesso ao cadastrar
- Exibição correta de todas as informações na lista
- Funcionalidade de exclusão operacional

### 2. Fluxo de Listagem de Cursos

**Caminho:** Tela Inicial → Listar Cursos

**Comportamentos esperados:**
- Exibição de todos os cursos cadastrados
- Formatação adequada das informações em layout de duas colunas
- Exibição de endereço para cursos presenciais
- Exibição de link de inscrição para cursos online
- Tratamento de lista vazia
- Layout responsivo e consistente

### 3. Fluxo de Exclusão de Curso

**Caminho:** Lista de Cursos → Botão Excluir → Confirmação

**Comportamentos esperados:**
- Remoção efetiva do curso da listagem
- Mensagem de confirmação antes da exclusão
- Feedback de sucesso após exclusão

### 3. Fluxo de Navegação

**Elementos de navegação:**
- Menu/botões para alternar entre telas
- Breadcrumbs ou indicação de localização
- Botões de ação (voltar, cadastrar, etc.)

## ⚠️ Pontos Críticos Identificados

### 1. Validações de Formulário (CRÍTICO)
**Problema:** Sistema permite salvar cursos sem validação adequada dos dados.

**Detalhes identificados:**
- Campos obrigatórios não são validados
- Aceita valores inválidos em todos os campos
- Permite datas inconsistentes (fim antes do início)
- Não valida formato de URLs/links
- Ausente limitação de caracteres

**Impacto:** Compromete integridade dos dados e experiência do usuário.

### 2. Funcionalidades de Gestão Incompletas
**Problemas identificados:**
- **Ausência de edição:** Não é possível editar cursos cadastrados
- **Exclusão não funcional:** Botão excluir não remove curso da listagem
- **Duplicação permitida:** É possível cadastrar cursos com mesmo nome

**Impacto:** Limita severamente a usabilidade para gestão de cursos.

### 3. Problemas de Exibição na Listagem (CONFIRMADO VISUALMENTE)
**Problemas identificados e confirmados:**
- **Informações importantes ocultas:** ✅ **CONFIRMADO** - Endereço e link NÃO são exibidos
- **Layout inconsistente:** ✅ **CONFIRMADO** - Cards com alturas muito diferentes
- **Quebra de layout:** ✅ **CONFIRMADO** - Textos longos deformam cards
- **Ausência de paginação:** 🆕 **NOVO** - Todos os cursos em uma única página
- **Responsividade:** ✅ **FUNCIONAL** - Desktop 2 colunas, Mobile 1 coluna
- **Elementos não clicáveis:** ✅ **CONFIRMADO** - Apenas botão excluir é interativo

**Detalhes observados nas imagens:**
- **Desktop (1680px):** Grid de 2 colunas funcionando bem
- **Mobile (375px):** Cards empilhados verticalmente (1 coluna)
- **Textos longos:** Causam cards com alturas desproporcionais  
- **Sem limitação:** Títulos e descrições podem ter tamanho excessivo
- **Sem paginação:** Lista cresce infinitamente sem controle
- **Informações ausentes:** Apenas tipo (badge) é mostrado, endereço/link ficam ocultos

**Impacto:** Layout inconsistente, informações críticas ausentes e possível problema de performance.
- **Ausência de paginação:** 🆕 **NOVO** - Todos os cursos em uma única página
- **Responsividade:** ✅ **FUNCIONAL** - Desktop 2 colunas, Mobile 1 coluna

**Detalhes observados nas imagens:**
- **Desktop (1680px):** Grid de 2 colunas funcionando bem
- **Mobile (375px):** Cards empilhados verticalmente (1 coluna)
- **Textos longos:** Causam cards com alturas desproporcionais
- **Sem limitação:** Títulos e descrições podem ter tamanho excessivo
- **Sem paginação:** Lista cresce infinitamente sem controle

**Impacto:** Layout inconsistente e possível problema de performance com muitos cursos.

### 4. Integridade de Dados
**Problemas identificados:**
- Dados inconsistentes são aceitos pelo sistema
- Falta de validação de unicidade
- Campos condicionais não são obrigatórios quando deveriam

**Impacto:** Compromete confiabilidade do sistema.

### 5. Ausência de Paginação (🆕 NOVO - Identificado visualmente)
**Problema:** Sistema não possui paginação para listagem de cursos.

**Detalhes observados:**
- Todos os cursos são exibidos em uma única página
- Lista pode crescer indefinidamente
- Sem controle de quantos itens exibir por página
- Possibilidade de impacto na performance com muitos cursos

**Impacto:** Performance e usabilidade comprometidas com crescimento da base de dados.

### 5. Funcionalidades Essenciais Ausentes (🆕 IDENTIFICADAS)
**Problemas:** Sistema carece de funcionalidades básicas de usabilidade.

**Funcionalidades ausentes identificadas:**
- **🔍 Busca/Filtro:** Impossibilidade de localizar curso específico
- **📋 Ordenação:** Sem critérios de organização da listagem
- **❓ Confirmação:** Exclusão sem modal de confirmação
- **⏳ Loading states:** Sem feedback durante operações
- **📋 Detalhes:** Não há visualização expandida de cursos
- **🧗 Breadcrumbs:** Ausência de indicação de navegação

**Impacto:** Funcionalidades básicas esperadas pelo usuário estão ausentes.

**Detalhes por funcionalidade:**
- **Busca (BUG016):** Com 10+ cursos, localizar um específico se torna difícil
- **Ordenação (BUG017):** Lista sem ordem lógica prejudica navegação
- **Confirmação (BUG018):** Risco de exclusão acidental
- **Estados de loading (BUG019):** Usuário não sabe se ação está processando

## 📊 Observações Visuais Confirmadas

### Layout da Listagem (Evidência Visual)

**✅ Informações corretamente exibidas:**
- Nome do curso (com destaque visual)
- Tipo do curso (Badge "Presencial" ou "Online" colorido)
- Descrição completa do curso
- Nome do instrutor
- Data de início e data de fim
- Número de vagas disponíveis
- Imagem de capa (quando fornecida)
- Botão "Excluir Curso" (vermelho, visível mas não funcional)

**❌ Informações importantes AUSENTES:**
- **Endereço completo** para cursos presenciais (apenas tipo é mostrado)
- **Link de inscrição** para cursos online (apenas tipo é mostrado)
- **Campos não clicáveis** - Nenhuma interação além do botão excluir
- **Detalhes adicionais** que poderiam ser úteis ao usuário

**❌ Problemas visuais confirmados:**
- Cards com alturas muito diferentes (variação de 200-600px aproximadamente)
- Textos longos em títulos e descrições quebram layout
- Ausência de truncamento de texto ("...")
- Falta de altura fixa ou mínima para os cards
- Espaçamento irregular entre elementos
- **Informações críticas ocultas** comprometem utilidade da listagem

**✅ Responsividade funcional:**
- **Desktop (1680px):** Grid 2 colunas, cards lado a lado
- **Mobile (375px):** Grid 1 coluna, cards empilhados
- Transição responsiva adequada
- Elementos se reorganizam corretamente

### Impacto Visual na Experiência
- **Positivo:** Informações são exibidas completamente
- **Negativo:** Layout desorganizado prejudica profissionalismo
- **Crítico:** Falta de paginação pode causar problemas de performance

## 🧐 Raciocínio Analítico e Decisões Tomadas

### Abordagem de Teste Utilizada

#### 1. Teste Exploratório Estruturado
**Decisão:** Iniciar com exploração livre da aplicação antes de criar casos de teste estruturados.

**Raciocínio:** 
- Permite descobrir funcionalidades não documentadas
- Identifica comportamentos inesperados rapidamente
- Fornece visão holística do sistema antes da análise detalhada

**Resultado:** Identificação de 14 bugs críticos que não seriam detectados apenas com testes baseados em requisitos.

#### 2. Priorização Baseada em Risco
**Decisão:** Focar primeiro em funcionalidades core (cadastro e listagem) antes de aspectos visuais.

**Raciocínio:**
- Funcionalidades básicas devem estar sólidas antes de refinar detalhes
- Bugs de validação têm impacto direto na integridade dos dados
- Problemas de usabilidade, embora importantes, não comprometem funcionalidade

**Resultado:** Identificação rápida de problemas estruturais graves.

#### 3. Análise de Fluxos Completos
**Decisão:** Testar jornadas completas do usuário, não apenas funcionalidades isoladas.

**Raciocínio:**
- Usuários reais executam fluxos completos
- Problemas de integração aparecem na jornada completa
- Identifica pontos de fricção na experiência

**Resultado:** Descoberta de que exclusão não funciona e ausência de edição limita usabilidade.

### Metodologia de Investigação de Defeitos

#### 1. Classificação Imediata por Impacto
**Processo:**
- **Crítica:** Funcionalidade não funciona (ex: exclusão)
- **Alta:** Compromete integridade (ex: falta de validação)
- **Média:** Afeta usabilidade (ex: duplicação permitida)
- **Baixa:** Problemas visuais (ex: alinhamento)

#### 2. Documentação Estruturada
**Decisão:** Padronizar formato de registro de bugs para facilitar correção.

**Elementos obrigatórios:**
- Passos detalhados para reprodução
- Resultado atual vs esperado
- Classificação de severidade e prioridade
- Sugestões de correção

#### 3. Análise de Causa Raiz
**Abordagem:** Para cada bug, investigar se é sintoma de problema maior.

**Exemplo:** Falta de validação em um campo indica provavel ausência de validação em todos os campos.

### Identificação de Vulnerabilidades

#### 1. Segurança de Dados
**Vulnerabilidade identificada:** Sistema aceita qualquer tipo de dado sem validação.

**Riscos:**
- Injeção de scripts maliciosos
- Corrupção de dados
- Ataques de negativação de serviço com dados excessivos

#### 2. Integridade do Sistema
**Vulnerabilidade:** Ausencia de validações permite estados inconsistentes.

**Cenarios de risco:**
- Datas inválidas podem causar erros em sistemas integrados
- Links quebrados prejudicam experiência
- Dados duplicados dificultam manutenção

#### 3. Usabilidade como Segurança
**Vulnerabilidade:** Funcionalidades não funcionais podem causar perda de dados.

**Exemplo:** Usuário tenta excluir curso, pensa que foi excluído, mas continua ativo.

### Tomada de Decisão em Cenários Reais

#### Cenário 1: Priorização de Bugs
**Situação:** Múltiplos bugs identificados, recursos limitados para correção.

**Decisão tomada:**
1. **Primeiro:** Corrigir exclusão não funcional (bloqueia funcionalidade)
2. **Segundo:** Implementar validações básicas (integridade)
3. **Terceiro:** Corrigir exibição de dados (usabilidade)
4. **Último:** Ajustes visuais (polêmento)

**Justificativa:** Impacto no usuário vs esforço de desenvolvimento.

#### Cenário 2: Comunicação de Riscos
**Situação:** Sistema em produção com bugs críticos identificados.

**Decisão de comunicação:**
- **Stakeholders técnicos:** Detalhes técnicos e passos para reprodução
- **Gestão:** Impacto no negócio e cronograma de correção
- **Usuários finais:** Orientações para evitar problemas até correção

### Forma de Investigação de Defeitos

#### Metodologia de 5W2H Aplicada

Para cada defeito identificado:

**What (O quê)?** Descrição clara do problema
**When (Último)?** Em que momento ocorre
**Where (Onde)?** Em qual parte do sistema
**Who (Quem)?** Que tipo de usuário é afetado
**Why (Por quê)?** Provável causa raiz
**How (Como)?** Passos para reproduzir
**How much (Quanto)?** Impacto estimado

#### Exemplo Prático - BUG012 (Exclusão não funciona)

**What:** Botão de exclusão não remove curso da listagem
**When:** Sempre que usuário clica em "Excluir curso"
**Where:** Na listagem de cursos, ação de exclusão
**Who:** Qualquer usuário tentando remover um curso
**Why:** Provável problema na implementação do backend ou desconexão frontend-backend
**How:** Cadastrar curso → Tentar excluir → Observar que permanece na lista
**How much:** Alto - Funcionalidade crítica não funcional

## 🎓 Cenarios de Teste Priorizados

### Alta Prioridade
1. **Cadastro com dados válidos** - Funcionalidade core
2. **Validação de campos obrigatórios** - Integridade de dados
3. **Listagem de cursos** - Visualização dos dados
4. **Estados vazios** - Experiência do usuário

### Média Prioridade
1. **Validações de formato** - Carga horária numérica
2. **Limites de caracteres** - Campos de texto
3. **Navegação entre telas** - Usabilidade
4. **Responsividade** - Compatibilidade

### Baixa Prioridade
1. **Performance com volume de dados** - Escalabilidade
2. **Caracteres especiais** - Edge cases
3. **Acessibilidade** - Inclusão
4. **SEO e metadados** - Otimização

## 🔍 Questões para Investigação

1. **Persistência de dados:** Os dados são salvos localmente ou em servidor?
2. **Edição/exclusão:** Existe funcionalidade para editar ou excluir cursos?
3. **Busca/filtros:** É possível filtrar ou buscar cursos específicos?
4. **Validações backend:** As validações são apenas frontend ou também backend?
5. **Limites:** Existe limite máximo de cursos ou caracteres por campo?

## 📊 Requisitos Funcionais Identificados

### RF01 - Cadastro de Curso
**Como** usuário  
**Quero** cadastrar um novo curso  
**Para** disponibilizar informações sobre cursos oferecidos

**Critérios de aceite:**
- Deve permitir inserir nome, descrição, carga horária e categoria
- Deve validar campos obrigatórios
- Deve exibir mensagem de sucesso após cadastro
- Deve limpar o formulário após cadastro bem-sucedido

### RF02 - Listagem de Cursos
**Como** usuário  
**Quero** visualizar todos os cursos cadastrados  
**Para** consultar as informações disponíveis

**Critérios de aceite:**
- Deve exibir todos os cursos em formato de lista
- Deve mostrar todas as informações cadastradas
- Deve exibir mensagem quando não houver cursos
- Deve manter formatação consistente

### RF03 - Navegação
**Como** usuário  
**Quero** navegar facilmente entre as funcionalidades  
**Para** usar o sistema de forma intuitiva

**Critérios de aceite:**
- Deve ter menu/botões claros para cada funcionalidade
- Deve permitir retornar à tela inicial
- Deve indicar a localização atual no sistema

## 🎨 Requisitos Não Funcionais

### RNF01 - Usabilidade
- Interface deve ser intuitiva e fácil de usar
- Feedback visual adequado para ações do usuário
- Mensagens de erro claras e orientativas

### RNF02 - Responsividade
- Deve funcionar adequadamente em dispositivos móveis
- Layout deve se adaptar a diferentes tamanhos de tela
- Elementos interativos devem ser acessíveis via touch

### RNF03 - Performance
- Tempo de resposta não deve exceder 3 segundos
- Carregamento de listas deve ser otimizado
- Interface deve ser responsiva durante operações

## 📝 Decisões Tomadas para Criação dos Testes

1. **Foco na funcionalidade core:** Priorização do cadastro e listagem como cenários principais
2. **Cobertura de validações:** Teste de todos os campos obrigatórios e opcionais
3. **Cenários de exceção:** Teste de estados vazios e dados inválidos
4. **Usabilidade:** Verificação da experiência do usuário em fluxos completos
5. **Compatibilidade:** Teste em diferentes resoluções/dispositivos

## 🔧 Ferramentas de Teste Utilizadas

- **Teste manual:** Exploração e validação funcional
- **Navegador:** Chrome/Edge para teste cross-browser
- **DevTools:** Inspeção de elementos e console
- **Screenshots:** Documentação visual dos testes
- **Gravação de tela:** Evidência de bugs e fluxos

---

**Próximos passos:**
1. Criação dos casos de teste estruturados
2. Execução sistemática dos cenários
3. Documentação de bugs e melhorias
4. Registro de evidências visuais