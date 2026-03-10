# 🐛 BUG019 - Ausência de estados de loading/feedback

## 📋 Informações Gerais
- **ID:** BUG019
- **Título:** Sistema não exibe estados de loading ou feedback visual durante operações
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Baixa 🟢
- **Prioridade:** Baixa

## 📝 Descrição
A aplicação não fornece feedback visual adequado durante operações como cadastro de curso, carregamento da listagem ou tentativas de exclusão, deixando o usuário sem saber se a ação está sendo processada.

## 🔄 Passos para Reproduzir
1. Acessar o formulário de cadastro de curso
2. Preencher os campos e clicar em "CADASTRAR CURSO"
3. Observar ausência de indicador de carregamento
4. Acessar listagem de cursos
5. Observar ausência de loading durante carregamento inicial
6. Tentar excluir um curso
7. Verificar falta de feedback visual durante processamento

## ❌ Resultado Atual
- Não há spinner ou indicador de carregamento
- Botões não mudam de estado durante processamento
- Usuário não sabe se ação foi registrada
- Interface "congelada" sem feedback
- Pode parecer que sistema travou ou não respondeu

## ✅ Resultado Esperado
- Spinner ou skeleton loading durante carregamento da listagem
- Botão "CADASTRAR CURSO" deve mostrar estado de loading
- Indicador visual durante processamento de ações
- Mensagens de feedback após conclusão das operações
- Estados intermediários claros para todas as ações

## 💥 Impacto no Usuário
- **Experiência:** Incerteza se ações foram processadas
- **Usabilidade:** Pode tentar clicar múltiplas vezes
- **Confiança:** Sistema parece "travado" ou não responsivo
- **Ansiedade:** Usuário não sabe se deve aguardar ou tentar novamente

## 📊 Classificações
- **Severidade:** Baixa - Não impede funcionalidade mas afeta experiência
- **Prioridade:** Baixa - Melhoria de UX para melhor feedback

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 🧪 Operações Testadas
- **Cadastro de curso:** Sem loading, sem feedback imediato
- **Carregamento da listagem:** Aparece instantaneamente ou sem indicação
- **Exclusão de curso:** Sem indicador durante tentativa
- **Navegação:** Transições sem estados intermediários

## 📸 Evidências
### Screenshots
- [ ] [Formulário sem estados de loading](screenshots/formulario-sem-loading.png)
- [ ] [Listagem sem skeleton/spinner](screenshots/listagem-sem-skeleton.png)
- [ ] [Botões sem estados de processamento](screenshots/botoes-sem-estados.png)

### Vídeos
- [x] [Vídeo demonstrativo do bug](videos/screen-capture%2520(4).webm)
- [ ] [Cadastro sem feedback visual](videos/cadastro-sem-feedback.mp4)
- [ ] [Navegação sem indicadores](videos/navegacao-sem-indicadores.mp4)

## 🛠️ Análise Técnica
### Possíveis Causas
1. **Frontend:** Estados de loading não implementados
2. **UX:** Design não considerou estados intermediários
3. **Desenvolvimento:** Foco apenas em estados finais (sucesso/erro)
4. **Performance:** Operações podem ser muito rápidas para mostrar loading

### Correções Necessárias
1. **Loading states:** Implementar spinners/skeletons durante carregamentos
2. **Button states:** Botões devem mostrar loading e ficar desabilitados
3. **Skeleton screens:** Placeholders durante carregamento da listagem
4. **Progress indicators:** Barras de progresso para operações longas
5. **Micro-interactions:** Animações sutis para feedback imediato
6. **Toast notifications:** Mensagens de sucesso/erro após operações

## 🔗 Casos de Teste Relacionados
- [CT027](../../test-cases/test-cases-link.md#ct027---estados-de-loading) - Estados de loading
- [CT028](../../test-cases/test-cases-link.md#ct028---feedback-visual-operações) - Feedback visual em operações

## 📋 Critérios de Aceitação para Correção
- [ ] Spinner durante carregamento da listagem
- [ ] Botões mostram estado de loading quando clicados
- [ ] Skeleton screens para conteúdo em carregamento
- [ ] Mensagens de feedback após operações
- [ ] Estados visuais consistentes em toda aplicação
- [ ] Performance de animações adequada

## 🎯 Estados de Loading Prioritários
1. **Cadastro:** Botão com spinner + "Cadastrando..."
2. **Listagem:** Skeleton cards durante carregamento
3. **Exclusão:** Botão com spinner + "Excluindo..."
4. **Geral:** Toast notifications para sucesso/erro

## 📊 Padrões de Feedback
- **Imediato:** Mudança visual no clique (0-100ms)
- **Rápido:** Spinner para operações até 2s
- **Longo:** Progress bar para operações >2s
- **Resultado:** Toast ou modal com resultado final

## 🎨 Especificações Visuais
- **Spinner:** Circular, cor primária, 20px
- **Skeleton:** Animação shimmer, cor cinza claro
- **Toast:** Canto superior direito, auto-dismiss 3s
- **Button loading:** Spinner + texto alterado

## ⚡ Impacto no Negócio
**BAIXO** - Melhoria de experiência do usuário que aumenta percepção de qualidade e responsividade da aplicação.

---
*Última atualização: 9 de março de 2026*
*Status: Melhoria de UX para melhor feedback e percepção de responsividade*