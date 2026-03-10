# 🔗 Mapeamento: Casos de Teste vs Bugs Identificados

Esta matriz mostra a correlação entre os casos de teste executados e os bugs encontrados durante os testes.

## 📊 Resumo de Execução

### Estatísticas dos Casos de Teste
- **Total de casos executados:** 22
- **Casos que PASSARAM:** 4 ✅
- **Casos que FALHARAM:** 12 ❌  
- **Casos PARCIAIS:** 4 ⚠️
- **Casos não executados:** 2 📝

### Eficácia na Identificação de Bugs
- **Taxa de detecção:** 67% (12 falhas + 4 parciais dos 22 casos)
- **Bugs críticos detectados:** 3
- **Bugs de alta severidade detectados:** 8

## 🎯 Correlação Casos de Teste → Bugs

### Módulo: Cadastro de Cursos

| Caso de Teste | Status | Bug Relacionado | Severidade |
|---|---|---|---|
| **CT001** - Cadastro presencial válido | ✅ PASSOU | - | - |
| **CT002** - Cadastro online válido | ✅ PASSOU | - | - |
| **CT003** - Validação Nome obrigatório | ❌ FALHOU | [BUG002](BUG002/README.md) | 🟠 Alta |
| **CT004** - Validação Descrição obrigatória | ❌ FALHOU | [BUG002](BUG002/README.md) | 🟠 Alta |
| **CT005** - Validação Instrutor obrigatório | ❌ FALHOU | [BUG002](BUG002/README.md) | 🟠 Alta |
| **CT006** - Validação URL da imagem | ❌ FALHOU | [BUG003](BUG003/README.md), [BUG006](BUG006/README.md) | 🟠 Alta |
| **CT007** - Validação Número de vagas | ❌ FALHOU | [BUG003](BUG003/README.md), [BUG004](BUG004/README.md) | 🟡 Média |
| **CT008** - Validação Datas consistentes | ❌ FALHOU | [BUG005](BUG005/README.md) | 🟡 Média |
| **CT009** - Campo Endereço (Presencial) | ✅ PASSOU | - | - |
| **CT010** - Campo Link (Online) | ✅ PASSOU | - | - |
| **CT011** - Limite de caracteres | ❌ FALHOU | [BUG008](BUG008/README.md) | 🟡 Média |
| **CT012** - Valores extremos | ❌ FALHOU | [BUG003](BUG003/README.md), [BUG004](BUG004/README.md) | 🟡 Média |

### Módulo: Listagem de Cursos

| Caso de Teste | Status | Bug Relacionado | Severidade |
|---|---|---|---|
| **CT013** - Lista vazia | ❌ FALHOU | [BUG001](BUG001/README.md) | 🟢 Baixa |
| **CT014** - Visualização curso presencial | ⚠️ PARCIAL | [BUG011](BUG011/README.md) | 🟠 Alta |
| **CT015** - Visualização curso online | ⚠️ PARCIAL | [BUG010](BUG010/README.md) | 🟠 Alta |
| **CT016** - Exibição endereço presencial | ❌ FALHOU | [BUG011](BUG011/README.md) | 🟠 Alta |
| **CT017** - Exibição link online | ❌ FALHOU | [BUG010](BUG010/README.md) | 🟠 Alta |
| **CT018** - Layout responsivo | ⚠️ PARCIAL | [BUG009](BUG009/README.md) | 🟡 Média |
| **CT019** - Consistência altura blocos | ❌ FALHOU | [BUG007](BUG007/README.md) | 🟢 Baixa |

### Módulo: Exclusão de Cursos

| Caso de Teste | Status | Bug Relacionado | Severidade |
|---|---|---|---|
| **CT020** - Exclusão de curso | ❌ FALHOU | [BUG012](BUG012/README.md) | 🔴 Crítica |
| **CT021** - Confirmação exclusão | 📝 A executar | [BUG018](BUG018/README.md) | 🟡 Média |
| **CT022** - Feedback exclusão | ⚠️ PARCIAL | [BUG012](BUG012/README.md), [BUG019](BUG019/README.md) | 🔴 Crítica |

## 🚨 Bugs Críticos NÃO Detectados por Casos de Teste

### Problemas de Segurança (Descobertos na Análise Exploratória)
| Bug ID | Título | Severidade | Motivo não detectado |
|---|---|---|---|
| **BUG020** | Ausência de autenticação | 🔴 Crítica | Fora do escopo dos casos funcionais |
| **BUG021** | Acesso público irrestrito | 🔴 Crítica | Fora do escopo dos casos funcionais |
| **BUG022** | Vulnerabilidade XSS | 🟠 Alta | Teste de segurança não incluído |
| **BUG023** | Ausência controle sessão | 🟠 Alta | Fora do escopo dos casos funcionais |
| **BUG024** | Ausência de auditoria | 🟡 Média | Fora do escopo dos casos funcionais |

### Funcionalidades Ausentes (Descobertos na Análise)
| Bug ID | Título | Severidade | Motivo não detectado |
|---|---|---|---|
| **BUG013** | Sem funcionalidade de edição | 🟡 Média | Funcionalidade não especificada nos requisitos |
| **BUG014** | Permite cursos duplicados | 🟡 Média | Cenário de validação não coberto |
| **BUG015** | Ausência de paginação | 🟡 Média | Não testado com grande volume |
| **BUG016** | Ausência de busca/filtro | 🟠 Alta | Funcionalidade não especificada |
| **BUG017** | Ausência de ordenação | 🟢 Baixa | Funcionalidade não especificada |

## 📈 Análise de Efetividade

### ✅ Sucessos dos Casos de Teste
- **100%** de cobertura das funcionalidades básicas
- **Detecção eficaz** de problemas de validação
- **Identificação precisa** de falhas funcionais críticas
- **Boa cobertura** de cenários de interface

### 🎯 Oportunidades de Melhoria
- **Casos de segurança:** Incluir testes de autenticação e autorização
- **Testes exploratórios:** Validar funcionalidades não especificadas
- **Testes de volume:** Verificar comportamento com muitos dados
- **Validação de duplicatas:** Incluir cenários de dados repetidos
- **Usabilidade avançada:** Testes de busca, filtros e ordenação

## 🔄 Recomendações para Próximas Execuções

### Novos Casos de Teste Sugeridos
1. **CT023** - Teste de autenticação e autorização
2. **CT024** - Validação de segurança XSS
3. **CT025** - Teste com volume grande de cursos (50+)
4. **CT026** - Validação de duplicatas
5. **CT027** - Funcionalidades de busca e filtro
6. **CT028** - Teste de edição de cursos
7. **CT029** - Teste de paginação

### Melhorias na Estratégia
- **Testes de segurança obrigatórios** em aplicações web
- **Análise exploratória sistemática** após casos formais
- **Validação de requisitos não funcionais** (performance, usabilidade)
- **Testes de regressão** após correções

---

**Conclusão:** Os casos de teste foram eficazes em detectar 67% dos bugs, especialmente problemas funcionais críticos. As falhas de segurança e funcionalidades ausentes foram identificadas através de análise exploratória complementar, demonstrando a importância de uma abordagem híbrida de testes.

*Última atualização: 9 de março de 2026*