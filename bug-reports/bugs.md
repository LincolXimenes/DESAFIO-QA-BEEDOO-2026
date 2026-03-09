# Relatório de Bugs Encontrados

Este documento contém o registro detalhado de todos os bugs identificados durante a análise e execução dos testes na aplicação de cadastro de cursos.

## 📊 Resumo dos Bugs

| ID | Título | Severidade | Status | Prioridade |
|---|---|---|---|---|
| BUG001 | Lista vazia sem mensagem informativa | Baixa | 🔍 Identificado | Média |
| BUG002 | Ausrência de validação de campos obrigatórios | Alta | 🔍 Identificado | Alta |
| BUG003 | Sistema aceita valores inválidos | Alta | 🔍 Identificado | Alta |
| BUG004 | Aceitação de tipos de dados incorretos | Média | 🔍 Identificado | Alta |
| BUG005 | Aceitação de datas inconsistentes | Média | 🔍 Identificado | Média |
| BUG006 | Aceitação de links inválidos | Média | 🔍 Identificado | Média |
| BUG007 | Blocos com tamanhos diferentes na listagem | Baixa | 🔍 Identificado | Baixa |
| BUG008 | Ausência de limitação de caracteres | Média | 🔍 Identificado | Média |
| BUG009 | Quebra de layout em algumas resoluções | Média | 🔍 Identificado | Média |
| BUG010 | Link de inscrição não é exibido (cursos online) | Alta | 🔍 Identificado | Alta |
| BUG011 | Endereço não é exibido (cursos presenciais) | Alta | 🔍 Identificado | Alta |
| BUG012 | Funcionalidade de exclusão não remove curso | Crítica | 🔍 Identificado | Alta |

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

## 📋 Template para Novos Bugs

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