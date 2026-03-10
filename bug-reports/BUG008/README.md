# 🐛 BUG008 - Ausência de limitação de caracteres

## 📋 Informações Gerais
- **ID:** BUG008
- **Título:** Campos de texto não possuem limitação de caracteres
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Média 🟡
- **Prioridade:** Média

## 📝 Descrição
Os campos de texto do formulário não possuem limite máximo de caracteres, permitindo entrada de textos extremamente longos que podem causar problemas de layout, performance e usabilidade.

## 🔄 Passos para Reproduzir
1. Acessar o formulário de cadastro de curso
2. Inserir textos muito longos nos campos:
   - Nome do curso com 500+ caracteres
   - Descrição com 5000+ caracteres
   - Instrutor com 200+ caracteres
3. Clicar em "CADASTRAR CURSO"
4. Observar que textos longos são aceitos
5. Verificar impacto na listagem

## ❌ Resultado Atual
- Campos aceitam textos de qualquer tamanho
- Não há contador de caracteres
- Textos muito longos podem quebrar layout
- Possível impacto na performance
- Listagem pode ficar desorganizada com textos longos

## ✅ Resultado Esperado
- Limite máximo de caracteres por campo
- Contador visual mostrando caracteres restantes
- Validação impedindo excesso de caracteres
- Mensagem informativa sobre limites
- Layout mantido mesmo com textos no limite

## 💥 Impacto no Usuário
- **Layout:** Textos longos podem quebrar apresentação
- **Usabilidade:** Dificuldade para ler informações muito extensas
- **Performance:** Textos muito grandes podem afetar carregamento
- **Experiência:** Falta de orientação sobre limites aceitos

## 📊 Classificações
- **Severidade:** Média - Pode afetar layout e usabilidade
- **Prioridade:** Média - Importante para manter qualidade dos dados

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 🧪 Testes Realizados
- **Nome do curso:** Testado com 500 caracteres (aceito)
- **Descrição:** Testado com 2000+ caracteres (aceito)
- **Instrutor:** Testado com 300 caracteres (aceito)
- **Endereço:** Testado com 1000 caracteres (aceito)

## 📸 Evidências
### Screenshots
- [x] [Screenshot do bug](screenshots/image.png)
- [ ] [Formulário com textos excessivamente longos](screenshots/textos-longos.png)
- [ ] [Layout quebrado por texto longo](screenshots/layout-quebrado.png)
- [ ] [Listagem com descrições muito extensas](screenshots/listagem-textos-longos.png)

### Vídeos
- [ ] [Inserção de textos longos sem limitação](videos/textos-sem-limite.mp4)

## 🛠️ Análise Técnica
### Possíveis Causas
1. **HTML:** Inputs sem atributo maxlength
2. **JavaScript:** Ausência de validação de tamanho
3. **CSS:** Layout não preparado para textos longos
4. **Backend:** API não valida tamanho dos campos

### Correções Necessárias
1. **Limites HTML:** Adicionar maxlength nos inputs
2. **Validação client-side:** JavaScript para verificar tamanhos
3. **Contador visual:** Mostrar caracteres restantes
4. **Validação server-side:** Backend deve limitar tamanhos
5. **Layout responsivo:** CSS preparado para textos no limite

## 🔗 Casos de Teste Relacionados
- [CT001](../../test-cases/test-cases-link.md#ct001---cadastro-básico-de-curso) - Cadastro básico de curso
- [CT007](../../test-cases/test-cases-link.md#ct007---validação-de-limites-de-caracteres) - Validação de limites de caracteres

## 📋 Critérios de Aceitação para Correção
- [ ] Limites máximos definidos para cada campo
- [ ] Contador de caracteres visível durante digitação
- [ ] Validação impedindo excesso de caracteres
- [ ] Mensagens informativas sobre limites
- [ ] Layout mantido com textos no limite máximo

## 🎯 Limites Sugeridos
- **Nome do curso:** 100 caracteres
- **Descrição:** 500 caracteres
- **Instrutor:** 80 caracteres
- **Endereço:** 200 caracteres
- **Link de inscrição:** 300 caracteres

## ⚡ Impacto no Negócio
**MÉDIO** - Textos excessivos podem comprometer apresentação e usabilidade, afetando credibilidade da plataforma.

---
*Última atualização: 9 de março de 2026*
*Status: Melhoria necessária para controle de qualidade dos dados*