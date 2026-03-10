# 🐛 BUG017 - Ausência de ordenação na listagem

## 📋 Informações Gerais
- **ID:** BUG017
- **Título:** Listagem não oferece opções de ordenação
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Baixa 🟢
- **Prioridade:** Média

## 📝 Descrição
Os cursos são exibidos sem ordem específica clara e não há opções para ordenar por diferentes critérios, dificultando organização e visualização lógica dos cursos cadastrados.

## 🔄 Passos para Reproduzir
1. Cadastrar múltiplos cursos em diferentes ordens
2. Acessar a listagem de cursos
3. Observar ordem aparentemente aleatória dos cursos
4. Procurar por controles de ordenação (dropdowns, botões, headers clicáveis)
5. Verificar ausência completa de opções de ordenação

## ❌ Resultado Atual
- Cursos aparecem sem ordem específica definida
- Não há controles para alterar ordenação
- Impossível organizar por critérios lógicos
- Ordem pode parecer aleatória para o usuário
- Dificuldade para localizar cursos seguindo padrões

## ✅ Resultado Esperado
- Ordenação padrão por ordem alfabética (A-Z)
- Opções de ordenação disponíveis:
  - Por nome (A-Z, Z-A)
  - Por data de início (mais recente, mais antiga)
  - Por tipo (Presencial primeiro, Online primeiro)
  - Por número de vagas (maior, menor)
  - Por data de cadastro (mais recente, mais antiga)
- Controles visuais claros para alterar ordenação
- Indicação da ordenação atual ativa

## 💥 Impacto no Usuário
- **Usabilidade:** Dificuldade para localizar cursos seguindo lógica
- **Organização:** Lista parece desorganizada e confusa
- **Experiência:** Falta de previsibilidade na apresentação
- **Produtividade:** Tempo extra para encontrar informações

## 📊 Classificações
- **Severidade:** Baixa - Não impede funcionalidade mas afeta organização
- **Prioridade:** Média - Melhoria importante para usabilidade

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 🧪 Padrões Observados
- **Ordem atual:** Parece seguir ordem de cadastro ou ID
- **Consistência:** Ordem se mantém entre recarregamentos
- **Lógica:** Não há padrão alfabético ou temporal óbvio
- **Expectativa:** Usuários esperam ordem alfabética por padrão

## 📸 Evidências
### Screenshots
- [ ] [Listagem sem ordenação específica](screenshots/listagem-sem-ordenacao.png)
- [ ] [Ausência de controles de ordenação](screenshots/sem-controles-ordenacao.png)
- [ ] [Comparação com padrões de UX](screenshots/comparacao-padrao-ordenacao.png)

### Vídeos
- [x] [Vídeo demonstrativo do bug](videos/screen-capture%20(2).webm)
- [x] [Demonstração da ausência de ordenação](videos/screen-capture%20(2).webm)
- [ ] [Navegação em lista sem ordenação](videos/navegacao-lista-desordenada.mp4)

## 🛠️ Análise Técnica
### Possíveis Causas
1. **Frontend:** Componentes de ordenação não implementados
2. **Backend:** API não suporta parâmetros de ordenação
3. **UX:** Design não considerou necessidade de ordenação
4. **Dados:** Ordem baseada em ID ou timestamp de criação

### Correções Necessárias
1. **Ordenação padrão:** Implementar ordem alfabética por nome
2. **Controles de ordenação:** Dropdown ou botões para escolher critério
3. **Backend:** Implementar parâmetros de ordenação na API
4. **Indicação visual:** Mostrar critério de ordenação ativo
5. **Persistência:** Manter ordenação escolhida durante sessão
6. **Responsividade:** Controles funcionais em mobile

## 🔗 Casos de Teste Relacionados
- [CT025](../../test-cases/test-cases-link.md#ct025---ordenação-de-cursos) - Ordenação de cursos
- [CT012](../../test-cases/test-cases-link.md#ct012---visualização-de-cursos-listagem) - Visualização de cursos na listagem

## 📋 Critérios de Aceitação para Correção
- [ ] Ordenação alfabética por padrão
- [ ] Múltiplas opções de ordenação disponíveis
- [ ] Controles intuitivos e acessíveis
- [ ] Indicação clara da ordenação ativa
- [ ] Funciona em diferentes resoluções
- [ ] Performance mantida com ordenação

## 🎯 Opções de Ordenação Prioritárias
1. **Nome:** A-Z (padrão), Z-A
2. **Data de início:** Mais próxima, mais distante
3. **Tipo:** Presencial primeiro, Online primeiro
4. **Vagas:** Mais vagas, menos vagas
5. **Cadastro:** Mais recente, mais antigo

## 📊 Implementação Sugerida
- **Interface:** Dropdown "Ordenar por: Nome (A-Z) ▼"
- **Posição:** Acima da listagem, alinhado à direita
- **Comportamento:** Reorganização imediata ao selecionar
- **Persistência:** Manter escolha durante navegação

## ⚡ Impacto no Negócio
**BAIXO** - Melhoria de usabilidade que torna a aplicação mais organizada e profissional.

---
*Última atualização: 9 de março de 2026*
*Status: Melhoria de usabilidade para melhor organização dos dados*