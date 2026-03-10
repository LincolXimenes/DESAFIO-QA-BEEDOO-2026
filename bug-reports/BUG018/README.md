# 🐛 BUG018 - Exclusão sem confirmação do usuário

## 📋 Informações Gerais
- **ID:** BUG018
- **Título:** Botão excluir não solicita confirmação antes da ação
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Média 🟡
- **Prioridade:** Média

## 📝 Descrição
O botão "Excluir Curso" tenta executar a ação imediatamente sem solicitar confirmação do usuário, criando alto risco de exclusão acidental de cursos. Apesar da funcionalidade de exclusão não estar operacional (BUG012), a ausência de confirmação representa uma falha grave de UX.

## 🔄 Passos para Reproduzir
1. Acessar a listagem de cursos
2. Localizar qualquer curso na lista
3. Clicar no botão "Excluir Curso"
4. Observar que não há modal de confirmação
5. Verificar que a ação tenta ser executada imediatamente

## ❌ Resultado Atual
- Clique no botão executa ação imediatamente
- Não há modal ou popup de confirmação
- Não há pergunta "Tem certeza?"
- Usuário não tem chance de cancelar ação
- Alto risco de exclusão acidental por engano

## ✅ Resultado Esperado
- Modal de confirmação deve aparecer ao clicar "Excluir"
- Pergunta clara: "Tem certeza que deseja excluir o curso [Nome]?"
- Dois botões distintos: "Cancelar" e "Confirmar Exclusão"
- Possibilidade de cancelar a ação
- Ação destrutiva só executada após confirmação explícita

## 💥 Impacto no Usuário
- **Segurança:** Alto risco de perda de dados por engano
- **Experiência:** Falta de controle sobre ações destrutivas
- **Confiança:** Usuário pode perder confiança no sistema
- **Usabilidade:** Não segue padrões de UX para ações perigosas

## 📊 Classificações
- **Severidade:** Média - Representa risco de perda acidental de dados
- **Prioridade:** Média - Importante para segurança das operações

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 🧪 Comportamento Atual
- **Clique no botão:** Ação imediata (falha, mas tentativa executada)
- **Feedback visual:** Apenas mensagem de erro/sucesso posterior
- **Cancelamento:** Impossível cancelar após clique
- **Prevenção:** Nenhuma barreira contra ações acidentais

## 📸 Evidências
### Screenshots
- [ ] [Botão excluir sem confirmação](screenshots/botao-excluir-sem-confirmacao.png)
- [ ] [Ausência de modal de confirmação](screenshots/sem-modal-confirmacao.png)
- [ ] [Comparação com padrões de UX](screenshots/comparacao-padroes-confirmacao.png)

### Vídeos
- [x] [Demonstração da exclusão sem confirmação](videos/screen-capture%2520(3).webm)
- [ ] [Clique em excluir sem confirmação](videos/clique-excluir-sem-confirmacao.mp4)

## 🛠️ Análise Técnica
### Possíveis Causas
1. **Frontend:** Evento de clique diretamente vinculado à ação
2. **UX:** Design não considerou confirmação para ações destrutivas
3. **Desenvolvimento:** Falta de implementação de modal de confirmação
4. **Padrões:** Não seguiu guidelines de UX para ações perigosas

### Correções Necessárias
1. **Modal de confirmação:** Implementar popup com pergunta clara
2. **Botões distintos:** "Cancelar" (secundário) e "Confirmar" (destrutivo)
3. **Informação contextual:** Mostrar nome do curso a ser excluído
4. **Estilo visual:** Botão de confirmação em cor de alerta (vermelho)
5. **Acessibilidade:** Suporte a ESC para cancelar e Enter para confirmar
6. **Foco:** Modal deve capturar foco e ser navegável por teclado

## 🔗 Casos de Teste Relacionados
- [CT026](../../test-cases/test-cases-link.md#ct026---confirmação-de-exclusão) - Confirmação de exclusão
- [CT011](../../test-cases/test-cases-link.md#ct011---exclusão-de-curso) - Exclusão de curso (relacionado)

## 📋 Critérios de Aceitação para Correção
- [ ] Modal de confirmação aparece ao clicar "Excluir"
- [ ] Pergunta clara com nome do curso
- [ ] Botões "Cancelar" e "Confirmar Exclusão" visíveis
- [ ] ESC cancela a ação
- [ ] Enter confirma apenas se botão de confirmação estiver em foco
- [ ] Modal é acessível por leitores de tela
- [ ] Funciona em mobile e desktop

## 🎯 Especificações do Modal
- **Título:** "Confirmar Exclusão"
- **Mensagem:** "Tem certeza que deseja excluir o curso '[Nome do Curso]'? Esta ação não pode ser desfeita."
- **Botão Cancelar:** Cinza, posição esquerda
- **Botão Confirmar:** Vermelho, posição direita, texto "Excluir Curso"
- **Comportamento:** Foco inicial no botão Cancelar

## 📋 Padrões de UX
- **Nielsen's Heuristics:** Prevenção de erros
- **Material Design:** Confirmation dialogs
- **WCAG:** Acessibilidade para ações destrutivas
- **Apple HIG:** Confirmação para ações irreversíveis

## ⚡ Impacto no Negócio
**MÉDIO** - Prevenção de perda acidental de dados aumenta confiança do usuário e reduz problemas de suporte.

---
*Última atualização: 9 de março de 2026*
*Status: Melhoria crítica de UX para prevenção de ações acidentais*