# 🐛 BUG016 - Ausência de funcionalidade de busca/filtro

## 📋 Informações Gerais
- **ID:** BUG016
- **Título:** Sistema não possui funcionalidade de busca ou filtro de cursos
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Alta 🟠
- **Prioridade:** Alta

## 📝 Descrição
A listagem de cursos não oferece nenhuma funcionalidade de busca ou filtro, dificultando significativamente a localização de cursos específicos, especialmente conforme o número de cursos cadastrados cresce.

## 🔄 Passos para Reproduzir
1. Acessar listagem com múltiplos cursos cadastrados
2. Procurar por campo de busca ou área de filtros na interface
3. Tentar localizar um curso específico manualmente
4. Observar ausência completa de funcionalidades de busca ou filtros
5. Verificar que é necessário percorrer toda a lista manualmente

## ❌ Resultado Atual
- Não existe campo de busca por nome do curso
- Não há filtros por tipo (Presencial/Online)
- Não há filtro por instrutor
- Não há filtro por período ou datas
- Não há filtro por disponibilidade de vagas
- Usuário deve percorrer manualmente toda a lista
- Localização de curso específico fica extremamente difícil

## ✅ Resultado Esperado
- Campo de busca por nome do curso com busca em tempo real
- Filtros por tipo de curso (Presencial/Online)
- Filtro por instrutor
- Filtro por período/data de início
- Filtro por disponibilidade de vagas
- Possibilidade de combinar múltiplos filtros
- Botão "Limpar filtros" para resetar busca

## 💥 Impacto no Usuário
- **Usabilidade:** Dificuldade significativa para encontrar cursos específicos
- **Produtividade:** Tempo perdido navegando lista completa manualmente
- **Experiência:** Frustração crescente ao não conseguir localizar rapidamente
- **Escalabilidade:** Problema se torna crítico com aumento do volume de dados

## 📊 Classificações
- **Severidade:** Alta - Impede localização eficiente de cursos
- **Prioridade:** Alta - Funcionalidade essencial para usabilidade

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 🧪 Cenários de Busca Testados
- **Busca por nome:** "JavaScript" (não disponível)
- **Filtro por tipo:** Online/Presencial (não disponível)
- **Filtro por instrutor:** "João Silva" (não disponível)
- **Busca combinada:** Múltiplos critérios (não disponível)

## 📸 Evidências
### Screenshots
- [ ] [Interface sem campo de busca](screenshots/interface-sem-busca.png)
- [ ] [Listagem sem filtros disponíveis](screenshots/listagem-sem-filtros.png)
- [ ] [Comparação com padrões de UX](screenshots/comparacao-padroes-busca.png)

### Vídeos
- [x] [Demonstração da ausência de busca/filtro](videos/screen-capture%20(2).webm)
- [ ] [Tentativa de localizar curso específico](videos/tentativa-localizar-curso.mp4)
- [ ] [Percorrer lista completa manualmente](videos/navegacao-manual-lista.mp4)

## 🛠️ Análise Técnica
### Possíveis Causas
1. **Frontend:** Componentes de busca e filtro não implementados
2. **Backend:** API não suporta parâmetros de busca/filtro
3. **UX:** Design não considerou necessidade de busca
4. **Desenvolvimento:** Funcionalidade não priorizada na implementação

### Correções Necessárias
1. **Campo de busca:** Input com busca em tempo real por nome
2. **Filtros básicos:** Dropdown para tipo, instrutor, período
3. **Backend:** Implementar endpoints com parâmetros de busca
4. **Interface:** Design claro e intuitivo para filtros
5. **Performance:** Busca otimizada para grandes volumes
6. **UX:** Indicação de resultados encontrados e filtros ativos

## 🔗 Casos de Teste Relacionados
- [CT023](../../test-cases/test-cases-link.md#ct023---busca-de-cursos-por-nome) - Busca de cursos por nome
- [CT024](../../test-cases/test-cases-link.md#ct024---filtros-de-cursos) - Filtros de cursos
- [CT012](../../test-cases/test-cases-link.md#ct012---visualização-de-cursos-listagem) - Visualização de cursos na listagem

## 📋 Critérios de Aceitação para Correção
- [ ] Campo de busca funcional por nome do curso
- [ ] Filtros por tipo, instrutor e período
- [ ] Busca em tempo real conforme digitação
- [ ] Combinação de múltiplos filtros
- [ ] Indicação de número de resultados encontrados
- [ ] Botão para limpar todos os filtros
- [ ] Performance mantida mesmo com muitos cursos

## 🎯 Funcionalidades Prioritárias
1. **Busca por nome:** Campo de texto com autocomplete
2. **Filtro por tipo:** Online/Presencial
3. **Filtro por instrutor:** Dropdown com instrutores disponíveis
4. **Filtro por data:** Período de início dos cursos
5. **Ordenação:** Por nome, data, tipo

## 📊 Cenários de Uso
- **Usuário busca curso específico:** "Curso de Python"
- **Filtro por modalidade:** Apenas cursos online
- **Busca por instrutor:** Todos os cursos de determinado professor
- **Combinação:** Cursos online de JavaScript em março

## ⚡ Impacto no Negócio
**ALTO** - Ausência de busca/filtros torna sistema impraticável com muitos cursos, prejudicando experiência do usuário e adoção da plataforma.

---
*Última atualização: 9 de março de 2026*
*Status: Funcionalidade crítica necessária para usabilidade adequada*