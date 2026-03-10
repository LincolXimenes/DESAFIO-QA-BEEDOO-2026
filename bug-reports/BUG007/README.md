# 🐛 BUG007 - Blocos com tamanhos diferentes na listagem

## 📋 Informações Gerais
- **ID:** BUG007
- **Título:** Blocos de cursos aparecem com tamanhos diferentes na listagem
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Baixa 🟢
- **Prioridade:** Baixa

## 📝 Descrição
Os cards/blocos dos cursos na listagem apresentam alturas e tamanhos inconsistentes, criando um layout irregular que prejudica a apresentação visual e a experiência do usuário.

## 🔄 Passos para Reproduzir
1. Cadastrar múltiplos cursos com diferentes quantidades de texto:
   - Um curso com descrição curta
   - Um curso com descrição longa
   - Cursos com nomes de diferentes tamanhos
2. Acessar a listagem de cursos
3. Observar as diferenças de altura dos cards
4. Verificar alinhamento inconsistente

## ❌ Resultado Atual
- Cards com alturas diferentes baseadas no conteúdo
- Layout irregular e desalinhado
- Aparência não profissional
- Quebra da consistência visual
- Dificuldade para escaneamento visual da lista

## ✅ Resultado Esperado
- Cards com altura uniforme e consistente
- Layout alinhado e organizado
- Truncamento de texto quando necessário
- Apresentação visual profissional
- Facilidade para comparar cursos rapidamente

## 💥 Impacto no Usuário
- **Estético:** Aparência não profissional da aplicação
- **Usabilidade:** Dificuldade para escanear a lista rapidamente
- **Experiência:** Layout desorganizado causa má impressão
- **Comparação:** Dificulta comparação visual entre cursos

## 📊 Classificações
- **Severidade:** Baixa - Problema visual que não impede funcionalidade
- **Prioridade:** Baixa - Melhoria estética para melhor apresentação

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 🧪 Cenários Observados
- **Descrição curta:** Card com altura menor
- **Descrição longa:** Card significativamente mais alto
- **Nome longo:** Quebra de linha afeta altura do card
- **Campos vazios:** Cards ainda menores que o padrão

## 📸 Evidências
### Screenshots
- [x] [Screenshot do bug](screenshots/image.png)
- [ ] [Listagem com cards de tamanhos diferentes](screenshots/cards-tamanhos-diferentes.png)
- [ ] [Comparação de alturas dos blocos](screenshots/comparacao-alturas.png)
- [ ] [Layout desalinhado](screenshots/layout-desalinhado.png)

### Vídeos
- [ ] [Navegação pela listagem irregular](videos/listagem-irregular.mp4)

## 🛠️ Análise Técnica
### Possíveis Causas
1. **CSS:** Ausência de altura fixa ou mínima nos cards
2. **Layout:** Flexbox ou grid sem propriedades de uniformização
3. **Conteúdo:** Texto de tamanhos variados sem truncamento
4. **Design:** Falta de padrão para dimensões dos cards

### Correções Necessárias
1. **Altura fixa:** Definir height ou min-height consistente
2. **Truncamento:** Limitar texto com ellipsis (...)
3. **CSS Grid/Flexbox:** Configurar para itens uniformes
4. **Design responsivo:** Manter consistência em diferentes telas
5. **Padrão visual:** Estabelecer guidelines para cards

## 🔗 Casos de Teste Relacionados
- [CT012](../../test-cases/test-cases-link.md#ct012---visualização-de-cursos-listagem) - Visualização de cursos na listagem
- [CT013](../../test-cases/test-cases-link.md#ct013---layout-responsivo) - Layout responsivo

## 📋 Critérios de Aceitação para Correção
- [ ] Cards com altura uniforme em todas as resoluções
- [ ] Truncamento automático de texto longo
- [ ] Layout alinhado e organizado
- [ ] Aparência consistente independente do conteúdo
- [ ] Funciona bem em diferentes tamanhos de tela

## ⚡ Impacto no Negócio
**BAIXO** - Melhoria estética que aumenta profissionalismo e credibilidade da aplicação.

---
*Última atualização: 9 de março de 2026*
*Status: Melhoria estética para melhor apresentação visual*