# 🐛 BUG004 - Aceitação de tipos de dados incorretos

## 📋 Informações Gerais
- **ID:** BUG004
- **Título:** Sistema aceita tipos de dados incorretos nos campos do formulário
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Média 🟡
- **Prioridade:** Média

## 📝 Descrição
O sistema aceita tipos de dados inadequados para campos específicos, permitindo entrada de texto onde deveria aceitar apenas números, ou outros tipos de incompatibilidade de formato.

## 🔄 Passos para Reproduzir
1. Acessar o formulário de cadastro de curso
2. Inserir tipos de dados incorretos:
   - Texto em campos numéricos (ex: "abc" em número de vagas)
   - Caracteres especiais em campos de nome
   - Formatos incorretos em campos específicos
3. Clicar em "CADASTRAR CURSO"
4. Observar que dados incorretos são aceitos

## ❌ Resultado Atual
- Campos numéricos aceitam texto
- Não há validação de formato de entrada
- Sistema salva dados com tipos incorretos
- Pode causar erros em processamento posterior

## ✅ Resultado Esperado
- Campos numéricos devem aceitar apenas números
- Validação de formato específico para cada tipo de campo
- Rejeição imediata de tipos incompatíveis
- Mensagens de erro claras sobre tipo esperado
- Impedimento de salvamento com tipos incorretos

## 💥 Impacto no Usuário
- **Funcionalidade:** Dados incorretos podem quebrar funcionalidades
- **Usabilidade:** Confusão sobre que tipo de dado inserir
- **Integridade:** Compromete a qualidade dos dados armazenados
- **Experiência:** Frustração ao não entender restrições

## 📊 Classificações
- **Severidade:** Média - Afeta qualidade dos dados mas não impede funcionamento
- **Prioridade:** Média - Importante para manter integridade dos dados

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 🧪 Campos Testados
- **Número de vagas:** Aceita texto "abc" quando deveria ser numérico
- **Nome do curso:** Aceita caracteres especiais inadequados
- **Campos de data:** Aceita formatos incorretos de data
- **Campos de URL:** Aceita texto simples ao invés de URLs válidas

## 📸 Evidências
### Screenshots
- [x] [Screenshot do bug](screenshots/image.png)
- [ ] [Campo numérico com texto](screenshots/campo-numerico-texto.png)
- [ ] [Tipos incorretos no formulário](screenshots/tipos-incorretos.png)
- [ ] [Dados salvos com tipos errados](screenshots/dados-tipos-errados.png)

### Vídeos
- [ ] [Demonstração de tipos incorretos](videos/tipos-dados-incorretos.mp4)

## 🛠️ Análise Técnica
### Possíveis Causas
1. **HTML:** Inputs sem type específico (text ao invés de number)
2. **JavaScript:** Falta de validação de tipos no frontend
3. **Backend:** Ausência de validação de tipos na API
4. **UI/UX:** Falta de indicação visual sobre tipo esperado

### Correções Necessárias
1. **Tipos HTML:** Usar input type apropriado (number, email, url, etc.)
2. **Validação client-side:** JavaScript para verificar tipos
3. **Validação server-side:** Backend deve validar tipos de dados
4. **Feedback visual:** Indicar tipo esperado para cada campo
5. **Mensagens específicas:** Erro personalizado para cada tipo

## 🔗 Casos de Teste Relacionados
- [CT001](../../test-cases/test-cases-link.md#ct001---cadastro-básico-de-curso) - Cadastro básico de curso
- [CT004](../../test-cases/test-cases-link.md#ct004---validação-de-tipos-específicos) - Validação de tipos específicos

## 📋 Critérios de Aceitação para Correção
- [ ] Inputs HTML com types apropriados
- [ ] Validação de tipos em tempo real
- [ ] Mensagens de erro específicas para cada tipo
- [ ] Indicação visual do tipo de dado esperado
- [ ] Funciona consistentemente em diferentes navegadores

## ⚡ Impacto no Negócio
**MÉDIO** - Pode causar inconsistências nos dados e potenciais erros em funcionalidades que dependem de tipos específicos.

---
*Última atualização: 9 de março de 2026*
*Status: Melhoria necessária para qualidade dos dados*