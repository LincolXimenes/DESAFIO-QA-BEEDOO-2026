# 🐛 BUG011 - Endereço não é exibido (cursos presenciais)

## 📋 Informações Gerais
- **ID:** BUG011
- **Título:** Cursos presenciais não exibem endereço na listagem
- **Data de identificação:** 9 de março de 2026
- **Identificado por:** Lincoln Ximenes
- **Status:** 🔍 Identificado
- **Severidade:** Alta 🟠
- **Prioridade:** Alta

## 📝 Descrição
Cursos cadastrados como "Presencial" não exibem o campo "Endereço" na listagem de cursos, impedindo que usuários interessados saibam onde o curso será realizado, tornando a informação inacessível.

## 🔄 Passos para Reproduzir
1. Cadastrar um curso selecionando tipo "Presencial"
2. Preencher o campo "Endereço" com informações válidas
3. Salvar o curso
4. Acessar a listagem de cursos
5. Localizar o curso presencial cadastrado
6. Observar que o endereço não é exibido no card/bloco

## ❌ Resultado Atual
- Campo "Endereço" não aparece na listagem
- Informação essencial para cursos presenciais fica oculta
- Usuários não sabem onde o curso será realizado
- Dados inseridos no cadastro são desperdiçados

## ✅ Resultado Esperado
- Endereço deve ser exibido claramente na listagem
- Informação deve ser facilmente localizável no card do curso
- Formatação adequada para endereços (ex: ícone de localização)
- Possível integração com mapas (clique para abrir no Google Maps)

## 💥 Impacto no Usuário
- **Funcionalidade:** Usuários não sabem onde comparecer ao curso
- **Crítico:** Informação essencial para cursos presenciais indisponível
- **Experiência:** Frustração ao não encontrar informação básica
- **Conversão:** Pode impedir inscrições por falta de informação

## 📊 Classificações
- **Severidade:** Alta - Compromete funcionalidade principal de cursos presenciais
- **Prioridade:** Alta - Deve ser corrigido urgentemente

## 🌐 Ambiente de Teste
- **URL:** https://creative-sherbet-a51eac.netlify.app/
- **Navegador:** Chrome/Edge
- **Dispositivo:** Desktop
- **Sistema Operacional:** Windows
- **Data do teste:** 9 de março de 2026

## 🧪 Cenário Testado
- **Tipo:** Presencial selecionado
- **Endereço inserido:** "Rua das Flores, 123 - Centro, São Paulo/SP"
- **Resultado cadastro:** Curso salvo com sucesso
- **Resultado listagem:** Endereço não exibido

## 📸 Evidências
### Screenshots
- [x] [Screenshot do bug](screenshots/image.png)
- [ ] [Formulário com endereço preenchido](screenshots/formulario-endereco-preenchido.png)
- [ ] [Curso presencial na listagem sem endereço](screenshots/listagem-sem-endereco.png)
- [ ] [Comparação: curso online vs presencial](screenshots/comparacao-online-presencial.png)

### Vídeos
- [ ] [Cadastro curso presencial com endereço](videos/cadastro-presencial-endereco.mp4)
- [ ] [Listagem sem exibir endereço](videos/listagem-endereco-oculto.mp4)

## 🛠️ Análise Técnica
### Possíveis Causas
1. **Frontend:** Componente de listagem não renderiza campo endereço
2. **Lógica:** Condicional para exibir endereço não implementada
3. **CSS:** Campo endereço pode estar oculto por estilo
4. **JavaScript:** Dados de endereço não são processados na exibição

### Correções Necessárias
1. **Condicional de exibição:** Mostrar endereço quando tipo = "Presencial"
2. **Layout do card:** Incluir área para exibição do endereço
3. **Formatação:** Apresentar endereço de forma clara e legível
4. **Ícones:** Adicionar ícone de localização para identificação visual
5. **Interação:** Opcional - link para abrir no Google Maps

## 🔗 Casos de Teste Relacionados
- [CT001](../../test-cases/test-cases-link.md#ct001---cadastro-básico-de-curso) - Cadastro básico de curso
- [CT009](../../test-cases/test-cases-link.md#ct009---exibição-de-endereço-curso-presencial) - Exibição de endereço curso presencial
- [CT012](../../test-cases/test-cases-link.md#ct012---visualização-de-cursos-listagem) - Visualização de cursos na listagem

## 📋 Critérios de Aceitação para Correção
- [ ] Endereço visível em cursos presenciais na listagem
- [ ] Campo não aparece em cursos online
- [ ] Formatação clara e legível
- [ ] Ícone ou indicação visual de localização
- [ ] Funciona em diferentes resoluções de tela

## ⚡ Impacto no Negócio
**ALTO** - Informação crítica para cursos presenciais não disponível, pode impedir inscrições e comprometer credibilidade.

---
*Última atualização: 9 de março de 2026*
*Status: Correção urgente necessária para funcionalidade de cursos presenciais*