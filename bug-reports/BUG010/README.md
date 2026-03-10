# 🔗 BUG010 - Link de inscrição não é exibido (cursos online)

## 📋 Informações Gerais
- **ID:** BUG010
- **Título:** Cursos online não exibem link de inscrição na listagem
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Alta 🟠
- **Prioridade:** Alta

## 📝 Descrição
Cursos cadastrados como "Online" não exibem o campo "Link de inscrição" na listagem, impedindo que usuários acessem o curso. Esta é uma falha crítica pois o link é a única forma de acesso ao curso online.

## 🔄 Passos para Reproduzir
1. Cadastrar curso selecionando tipo "Online"
2. Preencher o campo "Link de inscrição" com URL válida
3. Salvar o curso
4. Visualizar na listagem de cursos
5. Observar que o link não aparece na exibição do curso

## ❌ Resultado Atual
- Link de inscrição não é exibido na listagem
- Informação essencial fica inacessível ao usuário
- Campo é preenchido no cadastro mas não mostrado
- Curso online fica sem forma de acesso

## ✅ Resultado Esperado
- Link de inscrição deve ser exibido claramente na listagem
- Usuário deve poder clicar no link para acessar o curso
- Link deve ser visualmente destacado (botão ou link destacado)
- Validação se o link funciona ao clicar

## 💥 Impacto no Usuário
- **Funcional:** Impossibilita acesso ao curso online
- **Crítico:** Compromete o propósito principal da funcionalidade
- **Experiência:** Frustração ao não conseguir acessar curso
- **Negócio:** Curso online se torna inútil sem acesso

## 📊 Classificações
- **Severidade:** Alta - Funcionalidade principal comprometida
- **Prioridade:** Alta - Impede uso efetivo de cursos online

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop e Mobile
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 🧪 Dados de Teste
- **Tipo de curso:** Online
- **Link testado:** `https://exemplo.com/curso-online`
- **Resultado:** Link não aparece na listagem
- **Campo preenchido:** Confirmado durante cadastro

## 📸 Evidências
### Screenshots
- [x] [Screenshot do bug](screenshots/image.png)
- [ ] [Formulário com link preenchido](screenshots/cadastro-com-link.png)
- [ ] [Listagem sem link visível](screenshots/lista-sem-link.png)
- [ ] [Detalhes do curso online](screenshots/detalhes-curso-online.png)
- [ ] [Comparação: presencial vs online](screenshots/comparacao-tipos.png)

### Vídeos
- [ ] [Processo completo: cadastro → visualização](videos/cadastro-link-invisivel.mp4)
- [ ] [Navegação na listagem procurando link](videos/procurando-link.mp4)

## 🛠️ Análise Técnica
### Possíveis Causas
1. **Template de exibição:** Falta implementação do campo no template
2. **Lógica condicional:** Não há verificação de tipo "Online" na listagem
3. **Mapeamento de dados:** Backend não envia o campo para o frontend
4. **CSS:** Campo pode estar oculto ou com display:none

### Correções Necessárias
1. **Atualizar template:** Incluir exibição do link para cursos online
2. **Lógica condicional:** `if (curso.tipo === 'Online') { mostrar link }`
3. **Estilização:** Destacar visualmente o link de acesso
4. **Validação:** Verificar se URL é válida antes de exibir

## 🔄 Fluxo Esperado
```
Curso Online → Campo "Link" preenchido → Salvar → 
Listagem mostra: [Nome] [Descrição] [🔗 ACESSAR CURSO] → 
Clique abre curso em nova aba
```

## 🔗 Casos de Teste Relacionados
- [CT002](../../test-cases/test-cases-link.md#ct002---cadastro-de-curso-online) - Cadastro de curso online ✅ PASSOU
- [CT017](../../test-cases/test-cases-link.md#ct017---exibição-de-link---cursos-online) - Exibição de link - cursos online **❌ FALHOU**
- **Falha identificada:** Link de inscrição não é exibido na listagem de cursos online

## 🔗 Bugs Relacionados
- [BUG011](../BUG011/README.md) - Endereço não é exibido (cursos presenciais)

## 📋 Critérios de Aceitação para Correção
- [ ] Link de inscrição visível em cursos online
- [ ] Link clicável abre em nova aba
- [ ] Estilização adequada (botão ou link destacado)
- [ ] Validação de URL válida
- [ ] Funciona em diferentes navegadores/dispositivos

## ⚡ Impacto no Negócio
**ALTO** - Cursos online ficam completamente inacessíveis, tornando esta categoria de curso inútil na plataforma.

---
*Última atualização: 9 de março de 2026*
*Status: Correção prioritária para funcionalidade de cursos online*