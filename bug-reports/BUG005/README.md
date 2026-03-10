# 🐛 BUG005 - Aceitação de datas inconsistentes

## 📋 Informações Gerais
- **ID:** BUG005
- **Título:** Sistema aceita datas inconsistentes e inválidas
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Média 🟡
- **Prioridade:** Média

## 📝 Descrição
O sistema permite cadastrar cursos com datas inconsistentes, como data de início posterior à data de fim, datas passadas para novos cursos, ou formatos de data inválidos, comprometendo a lógica temporal dos cursos.

## 🔄 Passos para Reproduzir
1. Acessar o formulário de cadastro de curso
2. Inserir datas inconsistentes:
   - Data de início posterior à data de fim
   - Datas no passado para cursos futuros
   - Formatos de data inválidos (ex: 32/13/2026)
3. Clicar em "CADASTRAR CURSO"
4. Observar que o sistema aceita datas inconsistentes

## ❌ Resultado Atual
- Data de início pode ser posterior à data de fim
- Sistema aceita datas passadas sem aviso
- Formatos inválidos de data são aceitos
- Não há validação de lógica temporal
- Cursos aparecem na listagem com datas inconsistentes

## ✅ Resultado Esperado
- Data de início deve ser anterior à data de fim
- Validação de datas futuras para novos cursos
- Rejeição de formatos de data inválidos
- Mensagens de erro específicas para problemas de data
- Validação de intervalos de datas lógicos

## 💥 Impacto no Usuário
- **Lógica:** Cursos com períodos impossíveis ou inválidos
- **Confiabilidade:** Dados temporais inconsistentes no sistema
- **Experiência:** Confusão sobre validade dos cursos
- **Funcionalidade:** Possíveis erros em filtros por data

## 📊 Classificações
- **Severidade:** Média - Afeta lógica dos dados mas não impede funcionamento
- **Prioridade:** Média - Importante para consistência temporal

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 🧪 Cenários Testados
- **Data início > Data fim:** 15/04/2026 início, 10/04/2026 fim
- **Datas passadas:** 01/01/2020 para curso "novo"
- **Formatos inválidos:** 32/13/2026, 30/02/2026
- **Anos inconsistentes:** Datas muito distantes no futuro

## 📸 Evidências
### Screenshots
- [x] [Screenshot do bug](screenshots/image.png)
- [ ] [Formulário com datas inconsistentes](screenshots/datas-inconsistentes.png)
- [ ] [Curso salvo com data inválida](screenshots/curso-data-invalida.png)
- [ ] [Listagem com problemas de data](screenshots/listagem-datas-problemas.png)

### Vídeos
- [ ] [Cadastro com datas inválidas](videos/cadastro-datas-invalidas.mp4)

## 🛠️ Análise Técnica
### Possíveis Causas
1. **Frontend:** Ausência de validação de datas em JavaScript
2. **HTML:** Input de data sem validação min/max
3. **Backend:** API não valida lógica temporal
4. **Validação:** Falta de regras de negócio para datas

### Correções Necessárias
1. **Validação temporal:** Verificar data início < data fim
2. **Validação de futuro:** Datas não devem ser muito passadas
3. **Validação de formato:** Verificar formatos válidos de data
4. **Feedback específico:** Mensagens para cada tipo de erro de data
5. **Validação server-side:** Backend deve validar lógica temporal

## 🔗 Casos de Teste Relacionados
- [CT001](../../test-cases/test-cases-link.md#ct001---cadastro-básico-de-curso) - Cadastro básico de curso
- [CT005](../../test-cases/test-cases-link.md#ct005---validação-de-datas) - Validação de datas

## 📋 Critérios de Aceitação para Correção
- [ ] Data de início sempre anterior à data de fim
- [ ] Validação de datas futuras/válidas
- [ ] Rejeição de formatos inválidos
- [ ] Mensagens específicas para erros de data
- [ ] Validação funciona em diferentes fusos horários

## ⚡ Impacto no Negócio
**MÉDIO** - Datas inconsistentes podem confundir usuários sobre disponibilidade e validade dos cursos.

---
*Última atualização: 9 de março de 2026*
*Status: Melhoria necessária para consistência temporal dos dados*