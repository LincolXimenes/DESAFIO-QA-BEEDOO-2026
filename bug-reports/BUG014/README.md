# 🐛 BUG014 - Permite cadastro de cursos duplicados

## 📋 Informações Gerais
- **ID:** BUG014
- **Título:** Sistema permite cadastrar cursos com mesmo nome
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Alta 🟠
- **Prioridade:** Alta

## 📝 Descrição
O sistema não possui validação para impedir cadastro de cursos com nomes idênticos, permitindo duplicatas que podem causar confusão na gestão e visualização dos cursos.

## 🔄 Passos para Reproduzir
1. Cadastrar um curso com nome "Curso de JavaScript"
2. Preencher demais campos obrigatórios
3. Salvar o curso com sucesso
4. Cadastrar outro curso com exatamente o mesmo nome "Curso de JavaScript"
5. Observar que o sistema aceita e salva ambos os cursos
6. Verificar confusão na identificação dos cursos na listagem

## ❌ Resultado Atual
- Sistema aceita nomes duplicados sem nenhum aviso
- Múltiplos cursos com mesmo nome aparecem na listagem
- Confusão na identificação de cursos específicos
- Impossibilidade de distinguir cursos duplicados
- Não há validação de unicidade

## ✅ Resultado Esperado
- Validação de unicidade do nome do curso
- Mensagem de erro: "Já existe um curso com este nome"
- Impedimento do cadastro até que nome seja alterado
- Sugestão de nome alternativo ou edição do existente
- Opção para visualizar o curso existente

## 💥 Impacto no Usuário
- **Funcionalidade:** Dificulta gestão e identificação de cursos
- **Usabilidade:** Causa confusão na listagem de cursos
- **Integridade:** Compromete organização dos dados
- **Experiência:** Frustração ao não distinguir cursos duplicados

## 📊 Classificações
- **Severidade:** Alta - Compromete integridade e organização dos dados
- **Prioridade:** Alta - Importante para manter qualidade da base de dados

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 🧪 Dados de Teste
- **Nome duplicado testado:** "Curso de JavaScript"
- **Resultado primeiro cadastro:** Curso salvo com sucesso
- **Resultado segundo cadastro:** Curso duplicado também salvo
- **Comportamento:** Nenhum aviso ou impedimento apresentado

## 📸 Evidências
### Screenshots
- [x] [Screenshot do bug](screenshots/image.png)
- [ ] [Dois cursos com mesmo nome na listagem](screenshots/cursos-nomes-duplicados.png)
- [ ] [Formulário aceitando nome duplicado](screenshots/formulario-nome-duplicado.png)
- [ ] [Ausência de validação de unicidade](screenshots/sem-validacao-unicidade.png)

### Vídeos
- [ ] [Processo de cadastro de curso duplicado](videos/cadastro-curso-duplicado.mp4)

## 🛠️ Análise Técnica
### Possíveis Causas
1. **Frontend:** Ausência de validação de unicidade no JavaScript
2. **Backend:** API não verifica se nome já existe antes de salvar
3. **Banco de dados:** Falta de constraint de unicidade na coluna nome
4. **Validação:** Não há regra de negócio para impedir duplicatas

### Correções Necessárias
1. **Validação client-side:** Verificar nome antes do envio
2. **Validação server-side:** Backend deve rejeitar nomes duplicados
3. **Constraint DB:** Adicionar unicidade no banco de dados
4. **Feedback específico:** Mensagem clara sobre duplicação
5. **Alternativas:** Sugerir "Editar curso existente" ou variação do nome
6. **Auto-complete:** Mostrar cursos existentes durante digitação

## 🔗 Casos de Teste Relacionados
- [CT021](../../test-cases/test-cases-link.md#ct021---cadastro-de-curso-com-nome-duplicado) - Cadastro de curso com nome duplicado
- [CT001](../../test-cases/test-cases-link.md#ct001---cadastro-básico-de-curso) - Cadastro básico de curso (relacionado)

## 📋 Critérios de Aceitação para Correção
- [ ] Validação de unicidade em tempo real
- [ ] Mensagem de erro clara para nomes duplicados
- [ ] Impossibilidade de salvar com nome já existente
- [ ] Sugestão de alternativas ou edição do existente
- [ ] Funciona tanto no frontend quanto backend

## 🎯 Cenários de Validação
- **Nome exato:** "Curso de JavaScript" = "Curso de JavaScript"
- **Case insensitive:** "curso de javascript" = "Curso de JavaScript"
- **Espaços extras:** " Curso de JavaScript " = "Curso de JavaScript"
- **Caracteres especiais:** Normalização de acentos e pontuação

## ⚡ Impacto no Negócio
**ALTO** - Cursos duplicados comprometem organização, dificultam gestão e podem confundir usuários interessados.

---
*Última atualização: 9 de março de 2026*
*Status: Correção urgente necessária para integridade dos dados*