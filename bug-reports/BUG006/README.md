# 🐛 BUG006 - Aceitação de links inválidos

## 📋 Informações Gerais
- **ID:** BUG006
- **Título:** Sistema aceita links inválidos nos campos de URL
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Média 🟡
- **Prioridade:** Média

## 📝 Descrição
O sistema permite inserir URLs malformadas ou inválidas nos campos de link (como link de inscrição para cursos online), sem validação adequada de formato ou funcionalidade dos links.

## 🔄 Passos para Reproduzir
1. Acessar o formulário de cadastro de curso
2. Selecionar tipo "Online" para habilitar campo de link
3. Inserir URLs inválidas:
   - Texto simples sem protocolo: "google.com"
   - URLs malformadas: "htp://exemplo"
   - Links quebrados ou inexistentes
4. Clicar em "CADASTRAR CURSO"
5. Observar que links inválidos são aceitos

## ❌ Resultado Atual
- Sistema aceita qualquer texto como URL
- Não valida formato de protocolo (http/https)
- Links malformados são salvos no sistema
- Não há verificação se o link é funcional
- Links inválidos aparecem na listagem (quando exibidos)

## ✅ Resultado Esperado
- Validação de formato de URL (protocolo obrigatório)
- Verificação de URLs bem formadas
- Mensagem de erro para links inválidos
- Opcionalmente, verificação se link está acessível
- Normalização automática de URLs (adicionar https:// se necessário)

## 💥 Impacto no Usuário
- **Funcionalidade:** Usuários não conseguem acessar cursos online
- **Experiência:** Frustração ao clicar em links quebrados
- **Confiabilidade:** Sistema permite dados não funcionais
- **Usabilidade:** Confusão sobre formato correto de URL

## 📊 Classificações
- **Severidade:** Média - Afeta acesso aos cursos mas não quebra sistema
- **Prioridade:** Média - Importante para funcionalidade de cursos online

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 🧪 URLs Testadas
- **Sem protocolo:** "www.exemplo.com" (aceito incorretamente)
- **Protocolo inválido:** "ftp://exemplo.com" (deveria rejeitar)
- **Malformada:** "http:/exemplo.com" (aceito incorretamente)
- **Texto simples:** "link do curso" (aceito incorretamente)
- **Válida:** "https://www.exemplo.com" (deveria aceitar)

## 📸 Evidências
### Screenshots
- [x] [Screenshot do bug](screenshots/image.png)
- [ ] [Formulário com links inválidos](screenshots/links-invalidos.png)
- [ ] [Curso salvo com URL malformada](screenshots/curso-url-invalida.png)
- [ ] [Link não funcional na listagem](screenshots/link-nao-funcional.png)

### Vídeos
- [ ] [Cadastro com URLs inválidas](videos/cadastro-urls-invalidas.mp4)

## 🛠️ Análise Técnica
### Possíveis Causas
1. **Frontend:** Input text comum ao invés de type="url"
2. **JavaScript:** Falta de validação de formato de URL
3. **Backend:** API não valida formato de URLs
4. **Regex:** Ausência de expressão regular para validar URLs

### Correções Necessárias
1. **Input HTML:** Usar type="url" para validação básica
2. **Validação client-side:** Regex ou API para validar URLs
3. **Validação server-side:** Backend deve verificar formato
4. **Normalização:** Adicionar protocolo automaticamente se necessário
5. **Feedback específico:** Mensagem clara para URLs inválidas

## 🔗 Casos de Teste Relacionados
- [CT001](../../test-cases/test-cases-link.md#ct001---cadastro-básico-de-curso) - Cadastro básico de curso
- [CT006](../../test-cases/test-cases-link.md#ct006---validação-de-urls) - Validação de URLs
- [CT010](../../test-cases/test-cases-link.md#ct010---exibição-de-link-curso-online) - Exibição de link curso online

## 📋 Critérios de Aceitação para Correção
- [ ] Validação de formato de URL em tempo real
- [ ] Rejeição de URLs malformadas
- [ ] Normalização automática quando possível
- [ ] Mensagens de erro específicas para URLs
- [ ] Funciona com diferentes protocolos válidos

## ⚡ Impacto no Negócio
**MÉDIO** - Links inválidos impedem usuários de acessar cursos online, afetando a finalidade principal da funcionalidade.

---
*Última atualização: 9 de março de 2026*
*Status: Melhoria necessária para funcionalidade de cursos online*