# 🐛 Índice de Bugs - Sistema de Cadastro de Cursos

Este documento serve como índice centralizado de todos os bugs identificados durante os testes da aplicação. Cada bug possui documentação detalhada em pasta individual com evidências organizadas.

## 📋 Estrutura da Documentação

```
bug-reports/
├── BUG001/          # Lista vazia sem mensagem
│   ├── README.md    # Documentação completa
│   ├── screenshots/ # Evidências visuais
│   └── videos/     # Gravações de demonstração
├── BUG012/         # Exclusão não funciona
├── BUG020/         # Falha crítica de segurança
└── TEMPLATE-BUG.md # Template para novos bugs
```

## 🎯 Resumo Executivo

### Estatísticas Gerais
- **Total de bugs identificados:** 24
- **Bugs críticos:** 3 (BUG012, BUG020, BUG021)
- **Bugs de alta severidade:** 8
- **Bugs de média severidade:** 9
- **Bugs de baixa severidade:** 4

### Categorias de Problemas
- **🔒 Segurança:** 5 bugs (BUG020-BUG024)
- **⚙️ Funcionalidade:** 12 bugs (BUG002-BUG004, BUG010-BUG018)
- **🎨 Interface/UX:** 7 bugs (BUG001, BUG005-BUG009, BUG019)

## 📊 Índice de Bugs por Severidade

### 🔴 Bugs Críticos (3)
| ID | Título | Status | Pasta Individual |
|---|---|---|---|
| BUG012 | [Funcionalidade de exclusão não remove curso](BUG012/README.md) | 🔍 Identificado | [📁 BUG012/](BUG012/) |
| BUG020 | [Ausência de sistema de autenticação/autorização](BUG020/README.md) | 🔍 Identificado | [📁 BUG020/](BUG020/) |
| BUG021 | [Acesso público irrestrito a funcionalidades administrativas](BUG021/README.md) | 🔍 Identificado | [📁 BUG021/](BUG021/) |

### 🟠 Bugs de Alta Severidade (8)
| ID | Título | Status | Pasta Individual |
|---|---|---|---|
| BUG002 | [Ausência de validação de campos obrigatórios](BUG002/README.md) | 🔍 Identificado | [📁 BUG002/](BUG002/) |
| BUG003 | [Sistema aceita valores inválidos](BUG003/README.md) | 🔍 Identificado | [📁 BUG003/](BUG003/) |
| BUG010 | [Link de inscrição não é exibido (cursos online)](BUG010/README.md) | 🔍 Identificado | [📁 BUG010/](BUG010/) |
| BUG011 | [Endereço não é exibido (cursos presenciais)](BUG011/README.md) | 🔍 Identificado | [📁 BUG011/](BUG011/) |
| BUG016 | [Ausência de funcionalidade de busca/filtro](BUG016/README.md) | 🔍 Identificado | [📁 BUG016/](BUG016/) |
| BUG022 | [Vulnerabilidade XSS - Ausência de sanitização](BUG022/README.md) | 🔍 Identificado | [📁 BUG022/](BUG022/) |
| BUG023 | [Ausência de controle de sessão](BUG023/README.md) | 🔍 Identificado | [📁 BUG023/](BUG023/) |
| BUG014 | [Permite cadastro de cursos duplicados (mesmo nome)](BUG014/README.md) | 🔍 Identificado | [📁 BUG014/](BUG014/) |

### 🟡 Bugs de Média Severidade (9)  
| ID | Título | Status | Pasta Individual |
|---|---|---|---|
| BUG004 | [Aceitação de tipos de dados incorretos](BUG004/README.md) | 🔍 Identificado | [📁 BUG004/](BUG004/) |
| BUG005 | [Aceitação de datas inconsistentes](BUG005/README.md) | 🔍 Identificado | [📁 BUG005/](BUG005/) |
| BUG006 | [Aceitação de links inválidos](BUG006/README.md) | 🔍 Identificado | [📁 BUG006/](BUG006/) |
| BUG008 | [Ausência de limitação de caracteres](BUG008/README.md) | 🔍 Identificado | [📁 BUG008/](BUG008/) |
| BUG009 | [Quebra de layout em algumas resoluções](BUG009/README.md) | 🔍 Identificado | [📁 BUG009/](BUG009/) |
| BUG013 | [Ausência de funcionalidade de edição de cursos](BUG013/README.md) | 🔍 Identificado | [📁 BUG013/](BUG013/) |
| BUG015 | [Ausência de paginação na listagem de cursos](BUG015/README.md) | 🔍 Identificado | [📁 BUG015/](BUG015/) |
| BUG018 | [Exclusão sem confirmação do usuário](BUG018/README.md) | 🔍 Identificado | [📁 BUG018/](BUG018/) |
| BUG024 | [Ausência de auditoria e logs de ações](BUG024/README.md) | 🔍 Identificado | [📁 BUG024/](BUG024/) |

### 🟢 Bugs de Baixa Severidade (4)
| ID | Título | Status | Pasta Individual |
|---|---|---|---|
| BUG001 | [Lista vazia sem mensagem informativa](BUG001/README.md) | 🔍 Identificado | [📁 BUG001/](BUG001/) |
| BUG007 | [Blocos com tamanhos diferentes na listagem](BUG007/README.md) | 🔍 Identificado | [📁 BUG007/](BUG007/) |
| BUG017 | [Ausência de ordenação na listagem](BUG017/README.md) | 🔍 Identificado | [📁 BUG017/](BUG017/) |
| BUG019 | [Ausência de estados de loading/feedback](BUG019/README.md) | 🔍 Identificado | [📁 BUG019/](BUG019/) |

## 🚨 Alertas Críticos de Segurança

⚠️ **ATENÇÃO:** O sistema possui falhas críticas de segurança que tornam seu uso em produção **INACEITÁVEL**:

- **[BUG020](BUG020/README.md)** - Sistema completamente público sem autenticação
- **[BUG021](BUG021/README.md)** - Funcionalidades administrativas expostas publicamente  
- **[BUG022](BUG022/README.md)** - Vulnerabilidade XSS por falta de sanitização

## 📈 Análise de Impacto por Categoria

### 🔒 Problemas de Segurança (CRÍTICO)
- **Impacto:** Sistema não deve ser usado em produção
- **Ação necessária:** Correção obrigatória antes de qualquer deploy
- **Bugs relacionados:** BUG020, BUG021, BUG022, BUG023, BUG024

### ⚙️ Problemas Funcionais (ALTO)
- **Impacto:** Funcionalidades básicas não funcionam adequadamente
- **Ação necessária:** Correção prioritária para usabilidade
- **Bug mais crítico:** BUG012 (Exclusão não funciona)

### 🎨 Problemas de Interface (MÉDIO)
- **Impacto:** Experiência do usuário comprometida
- **Ação necessária:** Melhoria da usabilidade geral
- **Foco:** Layout responsivo e feedback visual

## 🛠️ Recomendações de Correção

### Fase 1 - Segurança (Obrigatória)
1. Implementar sistema de autenticação (BUG020)
2. Restringir acesso administrativo (BUG021)
3. Sanitizar entradas para prevenir XSS (BUG022)

### Fase 2 - Funcionalidades Críticas
1. Corrigir exclusão de cursos (BUG012)
2. Implementar validação de campos (BUG002)
3. Exibir links e endereços corretamente (BUG010, BUG011)

### Fase 3 - Melhorias de Usabilidade
1. Adicionar busca/filtros (BUG016)
2. Implementar paginação (BUG015)
3. Melhorar feedback visual (BUG001, BUG019)

## 📁 Como Navegar nos Bugs

Cada bug possui uma pasta individual com:
- **README.md** - Documentação completa e detalhada
- **screenshots/** - Evidências visuais do problema
- **videos/** - Gravações demonstrando o bug

**Exemplo de navegação:**
```bash
# Bug de alta prioridade
cd BUG012/
cat README.md  # Documentação completa
ls screenshots/  # Evidências visuais
ls videos/      # Demonstrações
```

## 📋 Template para Novos Bugs

Para reportar novos bugs, utilize o [template padrão](TEMPLATE-BUG.md) que garante documentação consistente e completa.

## 📝 Metodologia de Documentação

### Estrutura Padrão
Cada bug individual contém:
- **Informações gerais** (ID, severidade, prioridade)
- **Descrição detalhada** do problema
- **Passos de reprodução** específicos
- **Análise de impacto** no usuário e negócio
- **Evidências organizadas** (screenshots, vídeos)
- **Sugestões de correção** técnicas

### Critérios de Severidade
- **🔴 Crítica:** Sistema não funciona, falha completa, risco de segurança grave
- **🟠 Alta:** Funcionalidade principal comprometida, impede fluxos críticos
- **🟡 Média:** Funcionalidade secundária afetada, workaround disponível
- **🟢 Baixa:** Problemas cosméticos, não impedem uso do sistema

## 📞 Informações de Contato

**Testador responsável:** Lincoln Ximenes  
**Data da análise:** 9 de março de 2026  
**Aplicação testada:** https://creative-sherbet-a51eac.netlify.app/

---

*Este índice é mantido atualizado conforme novos bugs são identificados e bugs existentes são corrigidos. Consulte as pastas individuais para documentação técnica completa.*

## 🔗 Correlação com Casos de Teste

📊 **[Ver Mapeamento Completo](MAPEAMENTO-CASOS-BUGS.md)** - Correlação detalhada entre casos de teste executados e bugs identificados

### Resumo da Correlação
- **12 bugs detectados** através de casos de teste formais (❌ FALHOU)
- **4 bugs detectados** em execuções parciais (⚠️ PARCIAL)  
- **8 bugs identificados** apenas em análise exploratória (problemas de segurança e funcionalidades ausentes)
- **Taxa de detecção:** 67% através de casos estruturados

### Casos de Teste com Falhas Críticas
- **CT020** → [BUG012](BUG012/README.md) - Exclusão não funciona (🔴 Crítica)
- **CT003-005** → [BUG002](BUG002/README.md) - Validação ausente (🟠 Alta)  
- **CT017** → [BUG010](BUG010/README.md) - Link não exibido (🟠 Alta)
- **CT016** → [BUG011](BUG011/README.md) - Endereço não exibido (🟠 Alta)

### 🔴 Bugs Críticos (3)
| ID | Título | Status | Pasta Individual |
|---|---|---|---|
| BUG012 | [Funcionalidade de exclusão não remove curso](BUG012/README.md) | 🔍 Identificado | [📁 BUG012/](BUG012/) |
| BUG020 | [Ausência de sistema de autenticação/autorização](BUG020/README.md) | 🔍 Identificado | [📁 BUG020/](BUG020/) |
| BUG021 | [Acesso público irrestrito a funcionalidades administrativas](BUG021/README.md) | 🔍 Identificado | [📁 BUG021/](BUG021/) |

### 🟠 Bugs de Alta Severidade (8)
| ID | Título | Status | Pasta Individual |
|---|---|---|---|
| BUG002 | [Ausência de validação de campos obrigatórios](BUG002/README.md) | 🔍 Identificado | [📁 BUG002/](BUG002/) |
| BUG003 | [Sistema aceita valores inválidos](BUG003/README.md) | 🔍 Identificado | [📁 BUG003/](BUG003/) |
| BUG010 | [Link de inscrição não é exibido (cursos online)](BUG010/README.md) | 🔍 Identificado | [📁 BUG010/](BUG010/) |
| BUG011 | [Endereço não é exibido (cursos presenciais)](BUG011/README.md) | 🔍 Identificado | [📁 BUG011/](BUG011/) |
| BUG016 | [Ausência de funcionalidade de busca/filtro](BUG016/README.md) | 🔍 Identificado | [📁 BUG016/](BUG016/) |
| BUG022 | [Vulnerabilidade XSS - Ausência de sanitização](BUG022/README.md) | 🔍 Identificado | [📁 BUG022/](BUG022/) |
| BUG023 | [Ausência de controle de sessão](BUG023/README.md) | 🔍 Identificado | [📁 BUG023/](BUG023/) |
| BUG014 | [Permite cadastro de cursos duplicados (mesmo nome)](BUG014/README.md) | 🔍 Identificado | [📁 BUG014/](BUG014/) |

### 🟡 Bugs de Média Severidade (9)  
| ID | Título | Status | Pasta Individual |
|---|---|---|---|
| BUG004 | [Aceitação de tipos de dados incorretos](BUG004/README.md) | 🔍 Identificado | [📁 BUG004/](BUG004/) |
| BUG005 | [Aceitação de datas inconsistentes](BUG005/README.md) | 🔍 Identificado | [📁 BUG005/](BUG005/) |
| BUG006 | [Aceitação de links inválidos](BUG006/README.md) | 🔍 Identificado | [📁 BUG006/](BUG006/) |
| BUG008 | [Ausência de limitação de caracteres](BUG008/README.md) | 🔍 Identificado | [📁 BUG008/](BUG008/) |
| BUG009 | [Quebra de layout em algumas resoluções](BUG009/README.md) | 🔍 Identificado | [📁 BUG009/](BUG009/) |
| BUG013 | [Ausência de funcionalidade de edição de cursos](BUG013/README.md) | 🔍 Identificado | [📁 BUG013/](BUG013/) |
| BUG015 | [Ausência de paginação na listagem de cursos](BUG015/README.md) | 🔍 Identificado | [📁 BUG015/](BUG015/) |
| BUG018 | [Exclusão sem confirmação do usuário](BUG018/README.md) | 🔍 Identificado | [📁 BUG018/](BUG018/) |
| BUG024 | [Ausência de auditoria e logs de ações](BUG024/README.md) | 🔍 Identificado | [📁 BUG024/](BUG024/) |

### 🟢 Bugs de Baixa Severidade (4)
| ID | Título | Status | Pasta Individual |
|---|---|---|---|
| BUG001 | [Lista vazia sem mensagem informativa](BUG001/README.md) | 🔍 Identificado | [📁 BUG001/](BUG001/) |
| BUG007 | [Blocos com tamanhos diferentes na listagem](BUG007/README.md) | 🔍 Identificado | [📁 BUG007/](BUG007/) |
| BUG017 | [Ausência de ordenação na listagem](BUG017/README.md) | 🔍 Identificado | [📁 BUG017/](BUG017/) |
| BUG019 | [Ausência de estados de loading/feedback](BUG019/README.md) | 🔍 Identificado | [📁 BUG019/](BUG019/) |

## 🚨 Alertas Críticos de Segurança

⚠️ **ATENÇÃO:** O sistema possui falhas críticas de segurança que tornam seu uso em produção **INACEITÁVEL**:

- **[BUG020](BUG020/README.md)** - Sistema completamente público sem autenticação
- **[BUG021](BUG021/README.md)** - Funcionalidades administrativas expostas publicamente  
- **[BUG022](BUG022/README.md)** - Vulnerabilidade XSS por falta de sanitização

## 📈 Análise de Impacto por Categoria

### 🔒 Problemas de Segurança (CRÍTICO)
- **Impacto:** Sistema não deve ser usado em produção
- **Ação necessária:** Correção obrigatória antes de qualquer deploy
- **Bugs relacionados:** BUG020, BUG021, BUG022, BUG023, BUG024

### ⚙️ Problemas Funcionais (ALTO)
- **Impacto:** Funcionalidades básicas não funcionam adequadamente
- **Ação necessária:** Correção prioritária para usabilidade
- **Bug mais crítico:** BUG012 (Exclusão não funciona)

### 🎨 Problemas de Interface (MÉDIO)
- **Impacto:** Experiência do usuário comprometida
- **Ação necessária:** Melhoria da usabilidade geral
- **Foco:** Layout responsivo e feedback visual

## 🛠️ Recomendações de Correção

### Fase 1 - Segurança (Obrigatória)
1. Implementar sistema de autenticação (BUG020)
2. Restringir acesso administrativo (BUG021)
3. Sanitizar entradas para prevenir XSS (BUG022)

### Fase 2 - Funcionalidades Críticas
1. Corrigir exclusão de cursos (BUG012)
2. Implementar validação de campos (BUG002)
3. Exibir links e endereços corretamente (BUG010, BUG011)

### Fase 3 - Melhorias de Usabilidade
1. Adicionar busca/filtros (BUG016)
2. Implementar paginação (BUG015)
3. Melhorar feedback visual (BUG001, BUG019)

## 📁 Como Navegar nos Bugs

Cada bug possui uma pasta individual com:
- **README.md** - Documentação completa e detalhada
- **screenshots/** - Evidências visuais do problema
- **videos/** - Gravações demonstrando o bug

**Exemplo de navegação:**
```bash
# Bug de alta prioridade
cd BUG012/
cat README.md  # Documentação completa
ls screenshots/  # Evidências visuais
ls videos/      # Demonstrações
```

---

## 🐛 BUG001 - Lista vazia sem mensagem informativa

### Informações Gerais
- **ID:** BUG001
- **Título:** Lista vazia não exibe mensagem informativa para o usuário
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Baixa
- **Prioridade:** Média

### Descrição
Ao acessar a funcionalidade "Listar cursos" quando não existem cursos cadastrados no sistema, a aplicação exibe uma tela em branco ou lista vazia sem nenhuma mensagem informativa para o usuário.

### Passos para Reproduzir
1. Acessar a aplicação https://creative-sherbet-a51eac.netlify.app/
2. Garantir que não há cursos cadastrados no sistema
3. Clicar na opção "Listar cursos" ou navegar para a listagem
4. Observar o conteúdo exibido na tela

### Resultado Atual
- Tela exibe área de listagem vazia
- Não há mensagem indicando que a lista está vazia
- Usuário pode ficar confuso se a funcionalidade está funcionando

### Resultado Esperado
- Deve exibir mensagem clara indicando que não há cursos cadastrados
- Sugestões de mensagens:
  - "Nenhum curso cadastrado no momento"
  - "Sua lista de cursos está vazia. Que tal adicionar o primeiro?"
  - "Não há cursos para exibir. Clique aqui para cadastrar um novo curso"

### Impacto no Usuário
- **Usabilidade:** Usuário pode não entender se a funcionalidade está operacional
- **Experiência:** Pode causar confusão sobre o estado da aplicação
- **Confiança:** Usuário pode questionar se houve erro no carregamento

### Classificação de Severidade
**Baixa** - Funcionalidade principal não é impedida, mas afeta a experiência do usuário

### Classificação de Prioridade
**Média** - Deve ser corrigido para melhorar a experiência, mas não impede o uso do sistema

### Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

### Evidências
- [ ] Screenshot da tela vazia (a ser capturado)
- [ ] Vídeo demonstrando o comportamento (a ser gravado)

### Sugestões de Correção
1. **Implementar estado vazio:** Adicionar verificação se a lista está vazia
2. **Mensagem informativa:** Exibir texto explicativo quando não há dados
3. **Call-to-action:** Incluir botão ou link para cadastrar primeiro curso
4. **Ícone ilustrativo:** Adicionar ícone ou ilustração para melhor visual

### Casos de Teste Relacionados
- **CT011** - Visualização de lista vazia

### Observações Adicionais
- Este é um problema comum em aplicações e impacta diretamente na experiência do usuário
- A correção é relativamente simples mas melhora significativamente a usabilidade
- Recomenda-se seguir boas práticas de UX para estados vazios

---

## 🐛 BUG002 - Ausência de validação de campos obrigatórios

### Informações Gerais
- **ID:** BUG002
- **Título:** Sistema permite salvar cursos sem preenchimento de campos obrigatórios
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Alta
- **Prioridade:** Alta

### Descrição
O sistema permite cadastrar cursos deixando campos obrigatórios em branco, comprometendo a integridade dos dados e a experiência do usuário.

### Passos para Reproduzir
1. Acessar o formulário de cadastro de curso
2. Deixar campos essenciais vazios (nome, descrição, instrutor, etc.)
3. Clicar em "CADASTRAR CURSO"
4. Observar que o curso é salvo mesmo com campos vazios

### Resultado Atual
- Sistema aceita o cadastro sem validação
- Cursos são salvos com informações incompletas
- Não há feedback de erro para o usuário

### Resultado Esperado
- Sistema deve validar campos obrigatórios antes do envio
- Exibir mensagens de erro específicas para cada campo
- Impedir o cadastro até que todos os campos obrigatórios sejam preenchidos

### Impacto no Usuário
- **Integridade:** Dados inconsistentes no sistema
- **Usabilidade:** Cursos com informações incompletas na listagem
- **Confiabilidade:** Sistema parece aceitar dados inválidos

### Classificação
- **Severidade Alta:** Compromete a integridade dos dados
- **Prioridade Alta:** Deve ser corrigido urgentemente

---

## 🐛 BUG012 - Funcionalidade de exclusão não remove curso

### Informações Gerais
- **ID:** BUG012
- **Título:** Botão "Excluir curso" não remove o item da listagem
- **Data de identificação:** 9 de março de 2026
- **Status:** 🔍 Identificado
- **Severidade:** Crítica
- **Prioridade:** Alta

### Descrição
Ao clicar em "Excluir curso", o sistema exibe mensagem de sucesso, mas o curso permanece na listagem.

### Passos para Reproduzir
1. Acessar listagem de cursos
2. Clicar no botão "Excluir curso" em qualquer item
3. Confirmar a exclusão (se houver confirmação)
4. Observar a mensagem de sucesso
5. Verificar que o curso ainda aparece na lista

### Resultado Atual
- Mensagem de sucesso é exibida
- Curso permanece na listagem
- Funcionalidade não executa sua função principal

### Resultado Esperado
- Curso deve ser removido da listagem
- Mensagem de sucesso só deve aparecer após exclusão efetiva

### Impacto no Usuário
- **Crítico:** Funcionalidade básica não funciona
- **Confiabilidade:** Usuário perde confiança no sistema
- **Gestão:** Impossibilita remoção de cursos obsoletos

---

## 🐛 BUG010 - Link de inscrição não é exibido (cursos online)

### Informações Gerais
- **ID:** BUG010
- **Título:** Cursos online não exibem link de inscrição na listagem
- **Data de identificação:** 9 de março de 2026
- **Status:** 🔍 Identificado
- **Severidade:** Alta
- **Prioridade:** Alta

### Descrição
Cursos cadastrados como "Online" não exibem o campo "Link de inscrição" na listagem, impedindo que usuários acessem o curso.

### Passos para Reproduzir
1. Cadastrar curso selecionando tipo "Online"
2. Preencher o campo "Link de inscrição"
3. Salvar o curso
4. Visualizar na listagem
5. Observar que o link não aparece

### Resultado Atual
- Link de inscrição não é exibido na listagem
- Informação essencial fica inacessível

### Resultado Esperado
- Link de inscrição deve ser exibido claramente
- Usuário deve poder clicar no link para acessar o curso

### Impacto no Usuário
- **Funcional:** Impossibilita acesso ao curso online
- **Crítico:** Compromete o propósito principal da funcionalidade

---

## 🐛 BUG011 - Endereço não é exibido (cursos presenciais)

### Informações Gerais
- **ID:** BUG011
- **Título:** Cursos presenciais não exibem endereço na listagem
- **Data de identificação:** 9 de março de 2026
- **Status:** 🔍 Identificado
- **Severidade:** Alta
- **Prioridade:** Alta

### Descrição
Cursos cadastrados como "Presencial" não exibem o campo "Endereço" na listagem, impedindo que usuários saibam onde o curso será realizado.

### Impacto
- **Funcional:** Usuários não sabem onde comparecer
- **Crítico:** Informação essencial para cursos presenciais

---

## � BUG007 - Ausência de funcionalidade de edição de cursos

### Informações Gerais
- **ID:** BUG007
- **Título:** Sistema não possui funcionalidade para editar cursos cadastrados
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Média
- **Prioridade:** Média

### Descrição
O sistema permite apenas cadastrar e visualizar cursos, mas não oferece funcionalidade para editar informações de cursos já cadastrados, limitando a usabilidade para correções ou atualizações.

### Passos para Reproduzir
1. Cadastrar um curso com qualquer informação
2. Visualizar o curso na listagem
3. Procurar por botão/link de edição
4. Observar ausência da funcionalidade

### Resultado Atual
- Não existe botão ou funcionalidade de edição
- Cursos cadastrados não podem ser modificados
- Única opção seria exclusão e recadastro

### Resultado Esperado
- Botão "Editar" em cada curso na listagem
- Formulário de edição preenchido com dados atuais
- Possibilidade de modificar e salvar alterações

### Impacto no Usuário
- **Funcional:** Impossibilita correção de erros ou atualizações
- **Usabilidade:** Força recadastro completo para qualquer alteração

### Classificações
- **Severidade:** Média - Funcionalidade esperada não disponível
- **Prioridade:** Média - Importante para usabilidade completa

---

## 🐛 BUG008 - Permite cadastro de cursos duplicados

### Informações Gerais
- **ID:** BUG008
- **Título:** Sistema permite cadastrar cursos com mesmo nome
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Média
- **Prioridade:** Alta

### Descrição
O sistema não possui validação para impedir cadastro de cursos com nomes idênticos, permitindo duplicatas que podem causar confusão na gestão e visualização.

### Passos para Reproduzir
1. Cadastrar um curso com nome "Curso de JavaScript"
2. Cadastrar outro curso com exatamente o mesmo nome "Curso de JavaScript"
3. Observar que ambos são aceitos e listados

### Resultado Atual
- Sistema aceita nomes duplicados sem aviso
- Múltiplos cursos com mesmo nome na listagem
- Confusão na identificação de cursos

### Resultado Esperado
- Validação de unicidade do nome do curso
- Mensagem de erro: "Já existe um curso com este nome"
- Impedimento do cadastro duplicado

### Impacto no Usuário
- **Funcional:** Dificulta gestão e identificação de cursos
- **Usabilidade:** Causa confusão na listagem
- **Integridade:** Compromete organização dos dados

### Classificações
- **Severidade:** Média - Não impede funcionamento mas afeta qualidade
- **Prioridade:** Alta - Importante para integridade dos dados

### Sugestões de Correção
1. Validação no frontend antes do envio
2. Validação no backend para garantir unicidade
3. Mensagem clara de erro ao usuário
4. Opção de "Editar curso existente" como alternativa

---

## �📋 Template para Novos Bugs

### 🐛 BUG[XXX] - [Título do Bug]

#### Informações Gerais
- **ID:** BUG[XXX]
- **Título:** [Descrição breve do problema]
- **Data de identificação:** [Data]
- **Identificado por:** Lincoln Ximenes
- **Status:** [🔍 Identificado | 🧪 Em teste | ✅ Corrigido | ❌ Não reproduzido]
- **Severidade:** [Crítica | Alta | Média | Baixa]
- **Prioridade:** [Alta | Média | Baixa]

#### Descrição
[Descrição detalhada do problema identificado]

#### Passos para Reproduzir
1. [Passo 1]
2. [Passo 2]
3. [Passo 3]
4. [Resultado observado]

#### Resultado Atual
- [O que está acontecendo]

#### Resultado Esperado
- [O que deveria acontecer]

#### Impacto no Usuário
- **Funcional:** [Como afeta a funcionalidade]
- **Usabilidade:** [Como afeta a experiência]

#### Classificações
- **Severidade:** [Justificativa]
- **Prioridade:** [Justificativa]

#### Ambiente
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** [Navegador e versão]
- **Dispositivo:** [Desktop/Mobile]
- **Sistema:** [SO]

#### Evidências
- [ ] Screenshots
- [ ] Vídeos
- [ ] Logs (se aplicável)

---
---

## 🐛 BUG013 - Ausência de funcionalidade de edição de cursos

### Informações Gerais
- **ID:** BUG013
- **Título:** Sistema não possui funcionalidade para editar cursos cadastrados
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Média
- **Prioridade:** Média

### Descrição
O sistema permite apenas cadastrar e visualizar cursos, mas não oferece funcionalidade para editar informações de cursos já cadastrados, limitando a usabilidade para correções ou atualizações.

### Passos para Reproduzir
1. Cadastrar um curso com qualquer informação
2. Visualizar o curso na listagem
3. Procurar por botão/link de edição
4. Observar ausência da funcionalidade

### Resultado Atual
- Não existe botão ou funcionalidade de edição
- Cursos cadastrados não podem ser modificados
- Única opção seria exclusão e recadastro

### Resultado Esperado
- Botão "Editar" em cada curso na listagem
- Formulário de edição preenchido com dados atuais
- Possibilidade de modificar e salvar alterações

### Impacto no Usuário
- **Funcional:** Impossibilita correção de erros ou atualizações
- **Usabilidade:** Força recadastro completo para qualquer alteração
- **Produtividade:** Aumenta tempo para manutenção de dados

### Classificações
- **Severidade:** Média - Funcionalidade esperada não disponível
- **Prioridade:** Média - Importante para usabilidade completa

### Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

### Casos de Teste Relacionados
- **CT020** - Edição de curso cadastrado (caso inexistente)

### Sugestões de Correção
1. **Botão de edição:** Adicionar ícone/botão "Editar" em cada curso
2. **Formulário de edição:** Reutilizar formulário de cadastro preenchido
3. **Validação:** Manter mesmas validações do cadastro
4. **Feedback:** Mensagem de sucesso após edição

---

## 🐛 BUG014 - Permite cadastro de cursos duplicados

### Informações Gerais
- **ID:** BUG014
- **Título:** Sistema permite cadastrar cursos com mesmo nome
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Média
- **Prioridade:** Alta

### Descrição
O sistema não possui validação para impedir cadastro de cursos com nomes idênticos, permitindo duplicatas que podem causar confusão na gestão e visualização.

### Passos para Reproduzir
1. Cadastrar um curso com nome "Curso de JavaScript"
2. Cadastrar outro curso com exatamente o mesmo nome "Curso de JavaScript"
3. Observar que ambos são aceitos e listados
4. Verificar confusão na identificação dos cursos

### Resultado Atual
- Sistema aceita nomes duplicados sem aviso
- Múltiplos cursos com mesmo nome na listagem
- Confusão na identificação de cursos específicos
- Impossibilidade de distinguir cursos duplicados

### Resultado Esperado
- Validação de unicidade do nome do curso
- Mensagem de erro: "Já existe um curso com este nome"
- Impedimento do cadastro duplicado
- Sugestão de nome alternativo ou edição do existente

### Impacto no Usuário
- **Funcional:** Dificulta gestão e identificação de cursos
- **Usabilidade:** Causa confusão na listagem
- **Integridade:** Compromete organização dos dados
- **Experiência:** Frustração ao não distinguir cursos

### Classificações
- **Severidade:** Média - Não impede funcionamento mas afeta qualidade
- **Prioridade:** Alta - Importante para integridade dos dados

### Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

### Dados de Teste
- **Nome duplicado testado:** "Curso de JavaScript"
- **Resultado:** Ambos cursos foram cadastrados
- **Comportamento:** Nenhum aviso ou impedimento

### Casos de Teste Relacionados
- **CT021** - Cadastro de curso com nome duplicado
- **CT001** - Cadastro de curso com dados válidos (relacionado)

### Sugestões de Correção
1. **Validação no frontend:** Verificar antes do envio
2. **Validação no backend:** Garantir unicidade no servidor
3. **Mensagem clara:** Informar erro de duplicação
4. **Alternativas:** Sugerir "Editar curso existente" ou variação do nome
5. **Auto-complete:** Mostrar cursos existentes durante digitação

### Evidências
- [ ] Screenshot de dois cursos com mesmo nome na listagem
- [ ] Vídeo demonstrando cadastro duplicado
- [ ] Print da mensagem de erro esperada vs atual---

## 🐛 BUG015 - Ausência de paginação na listagem de cursos

### Informações Gerais
- **ID:** BUG015
- **Título:** Sistema não possui paginação para listagem de cursos
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Média
- **Prioridade:** Média

### Descrição
A listagem de cursos exibe todos os cursos cadastrados em uma única página, sem controle de paginação ou limite de itens por página, o que pode causar problemas de performance e usabilidade conforme a base de dados cresce.

### Passos para Reproduzir
1. Cadastrar vários cursos (10+ cursos)
2. Acessar a listagem de cursos
3. Observar que todos os cursos são exibidos simultaneamente
4. Verificar ausência de controles de paginação

### Resultado Atual
- Todos os cursos são exibidos em uma única página
- Lista pode crescer indefinidamente para baixo
- Não há controle de "itens por página"
- Ausência de navegação "Anterior/Próximo"
- Scroll da página pode ficar muito longo

### Resultado Esperado
- Sistema de paginação com controle de itens por página
- Botões "Anterior" e "Próximo" para navegação
- Indicação de "Página X de Y"
- Opção de escolher quantos itens exibir (ex: 6, 12, 24 por página)
- Melhor performance com grandes volumes

### Impacto no Usuário
- **Performance:** Página pode ficar lenta com muitos cursos
- **Usabilidade:** Scroll longo dificulta navegação
- **Experiência:** Localização de curso específico fica difícil
- **Escalabilidade:** Sistema não escala bem para grandes volumes

### Classificações
- **Severidade:** Média - Não impede funcionamento mas afeta escalabilidade
- **Prioridade:** Média - Importante para crescimento da plataforma

### Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivos testados:** Desktop (1680px), Mobile (375px)
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

### Evidência Visual Coletada
- ✅ Screenshots da listagem com múltiplos cursos
- ✅ Demonstração em diferentes resoluções
- ✅ Lista longa sem controles de paginação

### Casos de Teste Relacionados
- **CT022** - Visualização de lista com muitos cursos (novo caso)
- **CT012** - Visualização de curso cadastrado (relacionado)

### Sugestões de Correção
1. **Paginação simples:** Implementar "Anterior/Próximo" com 6-12 itens por página
2. **Controle de densidade:** Opções para escolher quantos itens exibir
3. **Indicação visual:** "Exibindo X-Y de Z cursos"
4. **Performance:** Carregamento sob demanda (lazy loading)
5. **Busca/filtro:** Implementar busca para localizar cursos específicos

### Cenários de Impacto
- **50+ cursos:** Página começa a ficar lenta para carregar
- **100+ cursos:** Scroll excessivo prejudica usabilidade
- **500+ cursos:** Impacto significativo na performance
- **Mobile:** Problema mais crítico devido ao espaço limitado

### Observações Adicionais
- Problema comum em aplicações que não consideram escalabilidade
- Solução relativamente simples mas crítica para sucesso da plataforma
- Deve ser considerado junto com funcionalidade de busca/filtros
- Importante testar performance com volumes realistas de dados---

## 🐛 BUG016 - Ausência de funcionalidade de busca/filtro

### Informações Gerais
- **ID:** BUG016
- **Título:** Sistema não possui funcionalidade de busca ou filtro de cursos
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Média
- **Prioridade:** Alta

### Descrição
A listagem de cursos não oferece nenhuma funcionalidade de busca ou filtro, dificultando a localização de cursos específicos, especialmente conforme o número de cursos cresce.

### Passos para Reproduzir
1. Acessar listagem com múltiplos cursos cadastrados
2. Procurar por campo de busca ou filtros
3. Tentar localizar um curso específico
4. Observar ausência de funcionalidades de busca

### Resultado Atual
- Não existe campo de busca
- Não há filtros por tipo, instrutor, data, etc.
- Usuário deve percorrer toda a lista manualmente
- Localização de curso fica mais difícil com muitos itens

### Resultado Esperado
- Campo de busca por nome do curso
- Filtros por tipo (Presencial/Online)
- Filtro por instrutor
- Filtro por período (datas)
- Filtro por disponibilidade de vagas
- Combinação de múltiplos filtros

### Impacto no Usuário
- **Usabilidade:** Dificuldade para encontrar cursos específicos
- **Produtividade:** Tempo perdido navegando lista completa
- **Experiência:** Frustração ao não conseguir localizar rapidamente
- **Escalabilidade:** Problema cresce com volume de dados

---

## 🐛 BUG017 - Ausência de ordenação na listagem

### Informações Gerais
- **ID:** BUG017
- **Título:** Listagem não oferece opções de ordenação
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Baixa
- **Prioridade:** Média

### Descrição
Os cursos são exibidos sem ordem específica clara e não há opções para ordenar por diferentes critérios, dificultando organização e visualização lógica.

### Resultado Esperado
- Ordenação por nome (A-Z, Z-A)
- Ordenação por data de início
- Ordenação por número de vagas
- Ordenação por tipo (Presencial/Online)
- Ordenação por data de cadastro

---

## 🐛 BUG018 - Exclusão sem confirmação do usuário

### Informações Gerais
- **ID:** BUG018
- **Título:** Botão excluir não solicita confirmação antes da ação
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Média
- **Prioridade:** Média

### Descrição
O botão "Excluir Curso" tenta executar a ação imediatamente sem solicitar confirmação do usuário, criando risco de exclusão acidental.

### Resultado Esperado
- Modal de confirmação: "Tem certeza que deseja excluir o curso [Nome]?"
- Botões "Cancelar" e "Confirmar Exclusão"
- Prevenção de ações acidentais

### Impacto
- **Segurança:** Risco de perda de dados por engano
- **UX:** Falta de confirmação para ações destrutivas
---

## 🔒 BUG020 - Ausência de sistema de autenticação/autorização

### Informações Gerais
- **ID:** BUG020
- **Título:** Sistema não possui controle de acesso, login ou autorização
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** **CRÍTICA**
- **Prioridade:** **CRÍTICA**

### Descrição
O sistema é completamente público, sem nenhum tipo de autenticação, autorização ou controle de acesso. Qualquer pessoa pode cadastrar, visualizar e tentar excluir cursos sem identificação.

### Passos para Reproduzir
1. Acessar a aplicação diretamente pela URL
2. Observar acesso imediato a todas as funcionalidades
3. Tentar cadastrar/excluir sem autenticação
4. Verificar ausência de tela de login ou cadastro

### Resultado Atual
- **Acesso total sem autenticação**
- Não existe tela de login
- Não existe cadastro de usuários
- Não existe controle de sessão
- Não existe diferenciação de permissões
- Qualquer pessoa pode modificar dados

### Resultado Esperado
- **Sistema de login obrigatório**
- Cadastro/registração de usuários
- Diferentes níveis de permissão (admin, editor, visualizador)
- Controle de sessão com timeout
- Logout seguro
- Tela de login como primeira interação

### Impacto de Segurança
- **CRÍTICO:** Qualquer pessoa pode modificar dados
- **Integridade:** Dados podem ser corrompidos por usuários mal-intencionados
- **Confidencialidade:** Informações sensíveis expostas publicamente
- **Responsabilidade:** Impossible rastrear quem fez o quê
- **Compliance:** Não atende padrões básicos de segurança

### Vulnerabilidades Identificadas
- **Acesso não autorizado** a funcionalidades administrativas
- **Modificação de dados** sem autenticação
- **Ausência de trilha de auditoria**
- **Exposição de informações** sem controle

---

## 🔒 BUG021 - Acesso público irrestrito a funcionalidades administrativas

### Informações Gerais
- **ID:** BUG021
- **Título:** Funcionalidades de cadastro e exclusão são públicas
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** **CRÍTICA**
- **Prioridade:** **CRÍTICA**

### Descrição
Funcionalidades administrativas como cadastro e exclusão de cursos estão expostas publicamente, permitindo que qualquer usuário anônimo execute ações que deveriam ser restritas a administradores.

### Resultado Atual
- **Cadastro público:** Qualquer pessoa pode criar cursos
- **Exclusão pública:** Tentativa de exclusão acessível a todos
- **Sem restrições de papel:** Não há diferenciação de permissões

### Resultado Esperado
- **Cadastro restrito** apenas a administradores/editores
- **Exclusão restrita** apenas a administradores
- **Visualização pública** da listagem (se desejado)
- **Controle de permissões** baseado em papéis

---

## 🔒 BUG022 - Vulnerabilidade XSS - Ausência de sanitização

### Informações Gerais
- **ID:** BUG022
- **Título:** Possível vulnerabilidade XSS por falta de sanitização de entrada
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** **ALTA**
- **Prioridade:** **ALTA**

### Descrição
O sistema aceita qualquer tipo de entrada sem validação ou sanitização, criando potencial para ataques XSS (Cross-Site Scripting) através de scripts maliciosos nos campos de texto.

### Teste de Vulnerabilidade
**Passos para testar:**
1. No campo "Nome do curso", inserir: `<script>alert('XSS')</script>`
2. No campo "Descrição", inserir: `<img src=x onerror=alert('XSS')>`
3. Cadastrar o curso
4. Verificar se scripts são executados na listagem

### Risco de Segurança
- **Execução de código malicioso** no navegador
- **Roubo de informações** de outros usuários
- **Redirecionamento** para sites maliciosos
- **Desfiguração** da aplicação

### Solução Esperada
- **Sanitização de entrada:** Escapar caracteres especiais HTML
- **Validação server-side:** Impedir scripts no backend
- **Content Security Policy (CSP):** Implementar cabeçalhos de segurança
- **Filtragem de conteúdo:** Remover/neutralizar tags perigosas

---

## 🔒 BUG023 - Ausência de controle de sessão

### Informações Gerais
- **ID:** BUG023
- **Título:** Sistema não possui gerenciamento de sessão de usuário
- **Data de identificação:** 9 de março de 2026
- **Status:** 🔍 Identificado
- **Severidade:** **ALTA**
- **Prioridade:** **ALTA**

### Descrição
Não existe controle de sessão, cookies de autenticação, timeout de inatividade ou logout seguro.

### Problemas Identificados
- **Sem timeout:** Sessão nunca expira
- **Sem cookies seguros:** Não há gerenciamento de estado
- **Sem logout:** Não há forma de encerrar sessão
- **Sem persistência segura:** Dados podem ficar expostos

---

## 🔒 BUG024 - Ausência de auditoria e logs de ações

### Informações Gerais
- **ID:** BUG024
- **Título:** Sistema não registra logs de ações de usuários
- **Data de identificação:** 9 de março de 2026
- **Status:** 🔍 Identificado
- **Severidade:** **MÉDIA**
- **Prioridade:** **MÉDIA**

### Descrição
Não há registro de quem cadastrou, editou ou tentou excluir cursos, impossibilitando rastreabilidade e auditoria.

### Logs Necessários
- **Ações de cadastro:** Quem, quando, o quê
- **Tentativas de exclusão:** Mesmo sem funcionar
- **Acessos à aplicação:** IPs, horários
- **Modificações:** Histórico de mudanças
## 📈 Critérios de Severidade

### 🔴 Crítica
- Sistema não funciona ou falha completamente
- Perda de dados
- Vulnerabilidades de segurança graves

### 🟠 Alta
- Funcionalidade principal não funciona
- Impede fluxos críticos do usuário
- Causa erros frequentes

### 🟡 Média
- Funcionalidade secundária não funciona adequadamente
- Impacta experiência do usuário
- Workaround disponível

### 🟢 Baixa
- Problemas cosméticos ou de usabilidade
- Não impede o uso do sistema
- Melhorias de interface

## 📊 Critérios de Prioridade

### 🚨 Alta
- Deve ser corrigido imediatamente
- Bloqueia funcionalidades críticas
- Impacta muitos usuários

### ⚡ Média
- Deve ser corrigido na próxima versão
- Melhora experiência do usuário
- Impacto moderado

### 📋 Baixa
- Pode ser corrigido quando houver tempo
- Melhorias de qualidade
- Impacto mínimo

---

**Status do documento:** 🔄 Em atualização constante
**Última atualização:** 9 de março de 2026

*Todos os bugs encontrados durante a execução dos testes serão documentados neste arquivo com o nível de detalhamento apropriado para facilitar a correção pelos desenvolvedores.*