# 📄 BUG015 - Ausência de paginação na listagem de cursos

## 📋 Informações Gerais
- **ID:** BUG015
- **Título:** Sistema não possui paginação para listagem de cursos
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Média 🟡
- **Prioridade:** Média

## 📝 Descrição
A listagem de cursos exibe todos os cursos cadastrados em uma única página, sem controle de paginação ou limite de itens por página, o que pode causar problemas de performance e usabilidade conforme a base de dados cresce.

## 🔄 Passos para Reproduzir
1. Cadastrar vários cursos (10+ cursos)
2. Acessar a listagem de cursos
3. Observar que todos os cursos são exibidos simultaneamente
4. Verificar ausência de controles de paginação

## ❌ Resultado Atual
- Todos os cursos são exibidos em uma única página
- Lista pode crescer indefinidamente para baixo
- Não há controle de "itens por página"
- Ausência de navegação "Anterior/Próximo"
- Scroll da página pode ficar muito longo
- Performance pode degradar com muitos itens

## ✅ Resultado Esperado
- Sistema de paginação com controle de itens por página
- Botões "Anterior" e "Próximo" para navegação
- Indicação de "Página X de Y"
- Opção de escolher quantos itens exibir (ex: 6, 12, 24 por página)
- Melhor performance com grandes volumes
- Navegação intuitiva entre páginas

## 💥 Impacto no Usuário
- **Performance:** Página pode ficar lenta com muitos cursos
- **Usabilidade:** Scroll longo dificulta navegação
- **Experiência:** Localização de curso específico fica difícil
- **Escalabilidade:** Sistema não escala bem para grandes volumes
- **Mobile:** Problema mais crítico devido ao espaço limitado

## 📊 Classificações
- **Severidade:** Média - Não impede funcionamento mas afeta escalabilidade
- **Prioridade:** Média - Importante para crescimento da plataforma

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivos testados:** Desktop (1680px), Mobile (375px)
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 🧪 Cenários de Teste
- **5 cursos:** Lista ainda gerenciável
- **10+ cursos:** Scroll começa a incomodar
- **20+ cursos:** Problema de usabilidade evidente
- **50+ cursos:** Performance pode degradar
- **Mobile:** Problema mais crítico em telas menores

## 📸 Evidências
### Screenshots
- [ ] [Listagem com múltiplos cursos](screenshots/lista-sem-paginacao.png)
- [ ] [Scroll longo demonstrando problema](screenshots/scroll-longo.png)
- [ ] [Comparação desktop vs mobile](screenshots/responsivo-sem-paginacao.png)
- [ ] [Mockup da solução esperada](screenshots/paginacao-esperada.png)

### Vídeos
- [x] [Demonstração do problema de paginação](videos/screen-capture%2520(2).webm)
- [ ] [Navegação em lista longa](videos/navegacao-lista-longa.mp4)
- [ ] [Demonstração em diferentes resoluções](videos/problema-responsivo.mp4)

## 🛠️ Análise Técnica
### Possíveis Causas
1. **Arquitetura simples:** Sistema não foi projetado para grandes volumes
2. **Falta de requisito:** Paginação não foi especificada inicialmente
3. **Implementação básica:** Foco apenas na funcionalidade core

### Correções Necessárias
1. **Paginação simples:** Implementar "Anterior/Próximo" com 6-12 itens por página
2. **Controle de densidade:** Opções para escolher quantos itens exibir
3. **Indicação visual:** "Exibindo X-Y de Z cursos"
4. **Performance:** Carregamento sob demanda (lazy loading)
5. **Persistência:** Manter página atual na navegação

## 🔄 Cenários de Impacto
- **10-20 cursos:** Começa a ficar desconfortável
- **20-50 cursos:** Problema de usabilidade claro
- **50+ cursos:** Impacto significativo na performance
- **100+ cursos:** Sistema praticamente inutilizável
- **Mobile:** Cada cenário é 2x mais crítico

## 🔗 Casos de Teste Relacionados
- [CT022](../../test-cases/test-cases-link.md#ct022---visualização-de-lista-com-muitos-cursos) - Visualização com volume grande de cursos (novo caso sugerido)
- [CT012](../../test-cases/test-cases-link.md#ct012---visualização-detalhada) - Visualização de curso cadastrado (relacionado)

## 🔗 Bugs Relacionados
- [BUG016](../BUG016/README.md) - Ausência de funcionalidade de busca/filtro
- [BUG017](../BUG017/README.md) - Ausência de ordenação na listagem

## 📋 Critérios de Aceitação para Correção
- [ ] Sistema de paginação implementado
- [ ] Controle de itens por página (6, 12, 24 opções)
- [ ] Navegação "Anterior" e "Próximo" funcional
- [ ] Indicador "Página X de Y" visível
- [ ] Performance mantida com grandes volumes
- [ ] Funciona bem em dispositivos móveis
- [ ] Estado da paginação persistente na sessão

## 📈 Impacto no Negócio
**MÉDIO** - Problema cresce exponencialmente com o sucesso da plataforma. Sistema com 100+ cursos se torna impraticável sem paginação.

## 📝 Observações Adicionais
- Problema comum em aplicações que não consideram escalabilidade desde o início
- Solução relativamente simples mas crítica para sucesso da plataforma
- Deve ser implementado junto com funcionalidade de busca/filtros para máxima eficácia
- Importante testar com volumes realistas de dados (50-100 cursos)
- Considerar lazy loading para otimização de performance

## 🔄 Sugestões de Melhoria
1. **Paginação inteligente:** Baseada no tamanho da tela
2. **Scroll infinito:** Como alternativa à paginação tradicional
3. **Cache local:** Para melhor performance na navegação
4. **Busca integrada:** Filtrar sem recarregar página
5. **Histórico:** Voltar à mesma página após visualizar curso

---
*Última atualização: 9 de março de 2026*
*Status: Importante para escalabilidade da plataforma*