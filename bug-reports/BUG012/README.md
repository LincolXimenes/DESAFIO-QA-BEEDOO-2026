# 🚫 BUG012 - Funcionalidade de exclusão não remove curso

## 📋 Informações Gerais
- **ID:** BUG012
- **Título:** Botão "Excluir curso" não remove o item da listagem
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Crítica 🔴
- **Prioridade:** Alta

## 📝 Descrição
Ao clicar em "Excluir curso", o sistema exibe mensagem de sucesso, mas o curso permanece na listagem. A funcionalidade principal de exclusão está completamente quebrada.

## 🔄 Passos para Reproduzir
1. Acessar listagem de cursos
2. Clicar no botão "Excluir curso" em qualquer item
3. Confirmar a exclusão (se houver confirmação)
4. Observar a mensagem de sucesso
5. Verificar que o curso ainda aparece na lista

## ❌ Resultado Atual
- Mensagem de sucesso é exibida
- Curso permanece na listagem
- Funcionalidade não executa sua função principal
- Comportamento inconsistente entre feedback e realidade

## ✅ Resultado Esperado
- Curso deve ser removido da listagem
- Mensagem de sucesso só deve aparecer após exclusão efetiva
- Lista deve ser atualizada instantaneamente
- Feedback visual da remoção (animação/transição)

## 💥 Impacto no Usuário
- **Crítico:** Funcionalidade básica não funciona
- **Confiabilidade:** Usuário perde confiança no sistema
- **Gestão:** Impossibilita remoção de cursos obsoletos
- **Experiência:** Frustração com comportamento enganoso

## 📊 Classificações
- **Severidade:** Crítica - Funcionalidade core completamente quebrada
- **Prioridade:** Alta - Impede gerenciamento adequado do sistema

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge (testado em ambos)
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 🧪 Dados de Teste
- **Cursos testados:** Múltiplos cursos de diferentes tipos
- **Comportamento:** Consistente - nenhuma exclusão funciona
- **Mensagens:** Sempre exibe "sucesso" independente do resultado

## 📸 Evidências
### Screenshots
- [x] [Screenshot do bug](screenshots/Captura%20de%20tela%202026-03-08%20223358.png)
- [ ] [Botão de exclusão na listagem](screenshots/botao-excluir.png)
- [ ] [Mensagem de sucesso enganosa](screenshots/mensagem-sucesso.png)
- [ ] [Curso ainda presente após "exclusão"](screenshots/curso-ainda-presente.png)
- [ ] [Listagem completa sem alteração](screenshots/lista-inalterada.png)

### Vídeos
- [ ] [Processo completo de tentativa de exclusão](videos/exclusao-nao-funciona.mp4)
- [ ] [Comparação antes/depois da "exclusão"](videos/antes-depois.mp4)

## 🛠️ Análise Técnica
### Possíveis Causas
1. **Frontend:** JavaScript não remove elemento do DOM
2. **Backend:** API de exclusão não implementada/funcionando
3. **Banco de dados:** Query de DELETE não executando
4. **Sincronização:** Problema entre frontend e backend

### Correções Necessárias
1. **Verificar API:** Implementar/corrigir endpoint de exclusão
2. **Validar frontend:** Garantir remoção do DOM após sucesso da API
3. **Tratamento de erros:** Exibir mensagem de erro quando exclusão falha
4. **Feedback visual:** Implementar loading durante operação

## 🔗 Casos de Teste Relacionados
- [CT020](../../test-cases/test-cases-link.md#ct020---exclusão-de-curso-da-listagem) - Exclusão de curso da listagem **❌ FALHOU**
- [CT021](../../test-cases/test-cases-link.md#ct021---confirmação-antes-da-exclusão) - Confirmação antes da exclusão 📝 A executar
- [CT022](../../test-cases/test-cases-link.md#ct022---mensagem-de-feedback-da-exclusão) - Mensagem de feedback da exclusão ⚠️ PARCIAL
- **Falha crítica identificada:** Funcionalidade de exclusão não remove o curso da listagem

## 🔗 Bugs Relacionados
- [BUG018](../BUG018/README.md) - Exclusão sem confirmação do usuário
- [BUG020](../BUG020/README.md) - Ausência de autenticação (agrava o problema)

## 📈 Impacto no Negócio
- **Gestão impossibilitada:** Administradores não podem remover conteúdo obsoleto
- **Acúmulo de dados:** Lista cresce indefinidamente
- **Experiência ruim:** Usuários perdem confiança na plataforma
- **Reputação:** Sistema parece não funcional

## ⚡ Prioridade de Correção
**ALTA** - Esta é uma funcionalidade básica esperada em qualquer sistema CRUD. A quebra impede operações administrativas essenciais.

---
*Última atualização: 9 de março de 2026*
*Status: Aguardando correção urgente*