# 🐛 BUG013 - Ausência de funcionalidade de edição de cursos

## 📋 Informações Gerais
- **ID:** BUG013
- **Título:** Sistema não possui funcionalidade para editar cursos cadastrados
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Média 🟡
- **Prioridade:** Média

## 📝 Descrição
O sistema permite apenas cadastrar e visualizar cursos, mas não oferece funcionalidade para editar informações de cursos já cadastrados, limitando a usabilidade para correções ou atualizações.

## 🔄 Passos para Reproduzir
1. Cadastrar um curso com qualquer informação
2. Visualizar o curso na listagem
3. Procurar por botão/link de edição no card do curso
4. Verificar menu de opções ou ações disponíveis
5. Observar ausência completa da funcionalidade de edição

## ❌ Resultado Atual
- Não existe botão ou funcionalidade de edição
- Cursos cadastrados não podem ser modificados
- Única opção seria exclusão e recadastro completo
- Interface não oferece acesso para alterar dados

## ✅ Resultado Esperado
- Botão "Editar" em cada curso na listagem
- Formulário de edição preenchido com dados atuais do curso
- Possibilidade de modificar qualquer campo
- Validação mantida igual ao cadastro
- Salvamento das alterações com feedback de sucesso

## 💥 Impacto no Usuário
- **Funcionalidade:** Impossibilita correção de erros ou atualizações
- **Usabilidade:** Força recadastro completo para qualquer alteração
- **Produtividade:** Aumenta tempo para manutenção de dados
- **Experiência:** Frustração ao não conseguir corrigir informações

## 📊 Classificações
- **Severidade:** Média - Funcionalidade esperada não disponível
- **Prioridade:** Média - Importante para usabilidade completa

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 🧪 Análise de Interface
- **Botões disponíveis:** Apenas "Excluir" (não funcional)
- **Ações de contexto:** Inexistentes
- **Menu de opções:** Não disponível
- **Ícones de ação:** Limitados ou ausentes

## 📸 Evidências
### Screenshots
- [x] [Screenshot do bug](screenshots/image.png)
- [ ] [Card de curso sem botão de edição](screenshots/curso-sem-edicao.png)
- [ ] [Interface limitada de ações](screenshots/interface-acoes-limitadas.png)
- [ ] [Comparação com padrões de UX](screenshots/comparacao-ux-padrao.png)

### Vídeos
- [ ] [Tentativa de encontrar funcionalidade de edição](videos/busca-funcionalidade-edicao.mp4)

## 🛠️ Análise Técnica
### Possíveis Causas
1. **Desenvolvimento:** Funcionalidade não implementada
2. **Roteamento:** Rotas de edição não criadas
3. **Interface:** Botões e componentes de edição não desenvolvidos
4. **Backend:** Endpoints para atualização podem não existir

### Correções Necessárias
1. **Botão de edição:** Adicionar ícone/botão "Editar" em cada curso
2. **Rota de edição:** Criar página/modal de edição
3. **Formulário de edição:** Reutilizar formulário de cadastro preenchido
4. **Backend:** Implementar endpoint PUT/PATCH para atualizações
5. **Validação:** Manter mesmas validações do cadastro
6. **Feedback:** Mensagem de sucesso após edição

## 🔗 Casos de Teste Relacionados
- [CT020](../../test-cases/test-cases-link.md#ct020---edição-de-curso-cadastrado) - Edição de curso cadastrado (caso inexistente)
- [CT001](../../test-cases/test-cases-link.md#ct001---cadastro-básico-de-curso) - Cadastro básico de curso (relacionado)

## 📋 Critérios de Aceitação para Correção
- [ ] Botão de edição visível em cada curso
- [ ] Formulário de edição preenchido com dados atuais
- [ ] Possibilidade de modificar todos os campos
- [ ] Validação funcionando corretamente
- [ ] Salvamento com feedback de sucesso
- [ ] Funciona em diferentes resoluções

## 🎯 Funcionalidades Esperadas
- **Edição in-line:** Opção para editar diretamente na listagem
- **Modal de edição:** Popup com formulário completo
- **Página dedicada:** Tela específica para edição
- **Histórico:** Opcional - log de alterações realizadas

## ⚡ Impacto no Negócio
**MÉDIO** - Ausência de edição força recadastro completo, reduzindo eficiência e satisfação dos usuários administradores.

---
*Última atualização: 9 de março de 2026*
*Status: Funcionalidade básica necessária para usabilidade completa*