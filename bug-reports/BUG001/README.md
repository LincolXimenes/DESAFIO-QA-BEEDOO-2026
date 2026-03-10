# 🐛 BUG001 - Lista vazia sem mensagem informativa

## 📋 Informações Gerais
- **ID:** BUG001
- **Título:** Lista vazia não exibe mensagem informativa para o usuário
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Baixa
- **Prioridade:** Média

## 📝 Descrição
Ao acessar a funcionalidade "Listar cursos" quando não existem cursos cadastrados no sistema, a aplicação exibe uma tela em branco ou lista vazia sem nenhuma mensagem informativa para o usuário.

## 🔄 Passos para Reproduzir
1. Acessar a aplicação https://creative-sherbet-a51eac.netlify.app/
2. Garantir que não há cursos cadastrados no sistema
3. Clicar na opção "Listar cursos" ou navegar para a listagem
4. Observar o conteúdo exibido na tela

## ❌ Resultado Atual
- Tela exibe área de listagem vazia
- Não há mensagem indicando que a lista está vazia
- Usuário pode ficar confuso se a funcionalidade está funcionando

## ✅ Resultado Esperado
- Deve exibir mensagem clara indicando que não há cursos cadastrados
- Sugestões de mensagens:
  - "Nenhum curso cadastrado no momento"
  - "Sua lista de cursos está vazia. Que tal adicionar o primeiro?"
  - "Não há cursos para exibir. Clique aqui para cadastrar um novo curso"

## 💥 Impacto no Usuário
- **Usabilidade:** Usuário pode não entender se a funcionalidade está operacional
- **Experiência:** Pode causar confusão sobre o estado da aplicação
- **Confiança:** Usuário pode questionar se houve erro no carregamento

## 📊 Classificações
- **Severidade:** Baixa - Funcionalidade principal não é impedida, mas afeta a experiência do usuário
- **Prioridade:** Média - Deve ser corrigido para melhorar a experiência, mas não impede o uso do sistema

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 📸 Evidências
### Screenshots
- [x] [Estado vazio da listagem](screenshots/image.png)
- [ ] [Tela vazia sem mensagem](screenshots/tela-vazia.png) *(a ser capturado)*
- [ ] [Comparação com estado ideal](screenshots/estado-esperado.png) *(mockup)*

### Vídeos
- [ ] [Demonstração do comportamento atual](videos/comportamento-atual.mp4) *(a ser gravado)*

## 🛠️ Sugestões de Correção
1. **Implementar estado vazio:** Adicionar verificação se a lista está vazia
2. **Mensagem informativa:** Exibir texto explicativo quando não há dados
3. **Call-to-action:** Incluir botão ou link para cadastrar primeiro curso
4. **Ícone ilustrativo:** Adicionar ícone ou ilustração para melhor visual

## 🔗 Casos de Teste Relacionados
- [CT013](../../test-cases/test-cases-link.md#ct013---visualização-de-lista-vazia) - Visualização de lista vazia **❌ FALHOU**
- **Falha identificada:** Lista vazia não exibe mensagem informativa

## 📝 Observações Adicionais
- Este é um problema comum em aplicações e impacta diretamente na experiência do usuário
- A correção é relativamente simples mas melhora significativamente a usabilidade
- Recomenda-se seguir boas práticas de UX para estados vazios

---
*Última atualização: 9 de março de 2026*