# 🐛 BUG002 - Ausência de validação de campos obrigatórios

## 📋 Informações Gerais
- **ID:** BUG002
- **Título:** Sistema permite salvar cursos sem preenchimento de campos obrigatórios
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Alta 🟠
- **Prioridade:** Alta

## 📝 Descrição
O sistema permite cadastrar cursos deixando campos obrigatórios em branco, comprometendo a integridade dos dados e a experiência do usuário. Não há validação adequada no formulário para garantir que informações essenciais sejam preenchidas.

## 🔄 Passos para Reproduzir
1. Acessar o formulário de cadastro de curso
2. Deixar campos essenciais vazios (nome, descrição, instrutor, etc.)
3. Clicar em "CADASTRAR CURSO"
4. Observar que o curso é salvo mesmo com campos vazios

## ❌ Resultado Atual
- Sistema aceita o cadastro sem validação
- Cursos são salvos com informações incompletas
- Não há feedback de erro para o usuário
- Campos vazios aparecem na listagem como espaços em branco

## ✅ Resultado Esperado
- Sistema deve validar campos obrigatórios antes do envio
- Exibir mensagens de erro específicas para cada campo
- Impedir o cadastro até que todos os campos obrigatórios sejam preenchidos
- Destacar visualmente campos com erro

## 💥 Impacto no Usuário
- **Integridade:** Dados inconsistentes no sistema
- **Usabilidade:** Cursos com informações incompletas na listagem
- **Confiabilidade:** Sistema parece aceitar dados inválidos
- **Experiência:** Confusão sobre quais campos são obrigatórios

## 📊 Classificações
- **Severidade:** Alta - Compromete a integridade dos dados
- **Prioridade:** Alta - Deve ser corrigido urgentemente

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 🧪 Campos Testados
- **Nome do curso:** Campo vazio aceito
- **Descrição:** Campo vazio aceito  
- **Instrutor:** Campo vazio aceito
- **Data de início:** Campo vazio aceito
- **Número de vagas:** Campo vazio aceito

## 📸 Evidências
### Screenshots
- [x] [Screenshot do bug](screenshots/image.png)
- [x] [Demonstração do problema de validação](screenshots/image.png)
- [ ] [Formulário com campos vazios](screenshots/campos-vazios.png)
- [ ] [Curso salvo sem informações](screenshots/curso-sem-dados.png)
- [ ] [Listagem com dados incompletos](screenshots/listagem-incompleta.png)

### Vídeos
- [ ] [Processo de cadastro sem validação](videos/cadastro-sem-validacao.mp4)

## 🛠️ Análise Técnica
### Possíveis Causas
1. **Frontend:** Ausência de validação JavaScript no formulário
2. **Backend:** API não valida dados antes de salvar
3. **UI/UX:** Falta indicação visual de campos obrigatórios

### Correções Necessárias
1. **Validação client-side:** JavaScript para verificar campos obrigatórios
2. **Validação server-side:** Backend deve rejeitar dados incompletos
3. **Feedback visual:** Destacar campos obrigatórios com asterisco (*)
4. **Mensagens de erro:** Específicas para cada tipo de validação

## 🔗 Casos de Teste Relacionados
- [CT003](../../test-cases/test-cases-link.md#ct003---validação-de-campos-obrigatórios---nome) - Validação de campos obrigatórios - Nome **❌ FALHOU**
- [CT004](../../test-cases/test-cases-link.md#ct004---validação-de-campos-obrigatórios---descrição) - Validação de campos obrigatórios - Descrição **❌ FALHOU**
- [CT005](../../test-cases/test-cases-link.md#ct005---validação-de-campos-obrigatórios---instrutor) - Validação de campos obrigatórios - Instrutor **❌ FALHOU**
- **Falhas identificadas:** Sistema permite cadastro sem preenchimento de campos obrigatórios

## 📋 Critérios de Aceitação para Correção
- [ ] Campos obrigatórios claramente identificados
- [ ] Validação em tempo real durante preenchimento
- [ ] Mensagens de erro específicas e claras
- [ ] Impossibilidade de salvar com campos vazios
- [ ] Funciona em diferentes navegadores

## ⚡ Impacto no Negócio
**ALTO** - Dados incompletos comprometem a qualidade do catálogo de cursos e podem causar problemas para usuários interessados.

---
*Última atualização: 9 de março de 2026*
*Status: Correção urgente necessária para integridade de dados*