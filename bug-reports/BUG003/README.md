# 🐛 BUG003 - Sistema aceita valores inválidos

## 📋 Informações Gerais
- **ID:** BUG003
- **Título:** Sistema aceita valores inválidos nos campos do formulário
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Alta 🟠
- **Prioridade:** Alta

## 📝 Descrição
O sistema permite inserir valores inválidos nos campos do formulário de cadastro de curso, não realizando validação adequada dos tipos de dados esperados para cada campo específico.

## 🔄 Passos para Reproduzir
1. Acessar o formulário de cadastro de curso
2. Inserir valores inadequados para cada tipo de campo:
   - Números negativos em "Número de vagas"
   - Textos muito longos em campos específicos
   - Caracteres especiais em campos que não deveriam aceitá-los
3. Clicar em "CADASTRAR CURSO"
4. Observar que o sistema aceita os valores inválidos

## ❌ Resultado Atual
- Sistema aceita números negativos para vagas
- Campos aceitam qualquer tipo de entrada
- Não há validação de formato ou tipo de dado
- Valores inválidos aparecem na listagem

## ✅ Resultado Esperado
- Validação de tipos de dados específicos para cada campo
- Rejeição de números negativos em campos numéricos
- Limitação de caracteres especiais onde inadequado
- Mensagens de erro específicas para cada tipo de validação
- Impedimento de cadastro com dados inválidos

## 💥 Impacto no Usuário
- **Integridade:** Dados inconsistentes e inválidos no sistema
- **Confiabilidade:** Sistema parece aceitar qualquer entrada
- **Experiência:** Confusão sobre quais valores são aceitáveis
- **Funcionalidade:** Possíveis erros em funcionalidades que dependem de dados válidos

## 📊 Classificações
- **Severidade:** Alta - Compromete a integridade e validação dos dados
- **Prioridade:** Alta - Deve ser corrigido urgentemente

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 🧪 Valores Testados
- **Número de vagas:** Valores negativos aceitos (-5, -10)
- **Nome do curso:** Caracteres especiais não validados
- **Campos de texto:** Comprimento excessivo aceito
- **Campos numéricos:** Tipos incorretos de dados aceitos

## 📸 Evidências
### Screenshots
- [x] [Screenshot do bug](screenshots/image.png)
- [ ] [Formulário com valores inválidos](screenshots/valores-invalidos.png)
- [ ] [Curso salvo com dados incorretos](screenshots/curso-dados-incorretos.png)
- [ ] [Listagem com valores inválidos](screenshots/listagem-valores-invalidos.png)

### Vídeos
- [ ] [Processo de cadastro com valores inválidos](videos/cadastro-valores-invalidos.mp4)

## 🛠️ Análise Técnica
### Possíveis Causas
1. **Frontend:** Ausência de validação de tipos no JavaScript
2. **Backend:** API não valida tipos de dados antes de salvar
3. **Validação:** Falta de regras específicas para cada campo

### Correções Necessárias
1. **Validação client-side:** JavaScript para verificar tipos de dados
2. **Validação server-side:** Backend deve validar tipos antes de salvar
3. **Regras específicas:** Definir validações para cada campo
4. **Mensagens de erro:** Feedback específico para cada tipo de erro

## 🔗 Casos de Teste Relacionados
- [CT006](../../test-cases/test-cases-link.md#ct006---validação-de-formato---url-da-imagem) - Validação de formato - URL da imagem **❌ FALHOU**
- [CT007](../../test-cases/test-cases-link.md#ct007---validação-de-formato---número-de-vagas) - Validação de formato - Número de vagas **❌ FALHOU**
- [CT012](../../test-cases/test-cases-link.md#ct012---cadastro-com-valores-extremos) - Cadastro com valores extremos **❌ FALHOU**
- **Falhas identificadas:** Sistema aceita valores inválidos sem validação adequada

## 📋 Critérios de Aceitação para Correção
- [ ] Validação de tipos de dados em tempo real
- [ ] Rejeição de valores negativos em campos numéricos
- [ ] Mensagens de erro específicas e claras
- [ ] Impossibilidade de salvar com dados inválidos
- [ ] Funciona em diferentes navegadores

## ⚡ Impacto no Negócio
**ALTO** - Dados inválidos comprometem a integridade do sistema e podem causar erros em funcionalidades dependentes.

---
*Última atualização: 9 de março de 2026*
*Status: Correção urgente necessária para integridade de dados*