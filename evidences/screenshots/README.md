# Screenshots - Evidências dos Testes

Esta pasta armazena todas as capturas de tela (screenshots) coletadas durante a execução dos testes da aplicação de cadastro de cursos.

## 📁 Organização dos Arquivos

### Nomenclatura Padrão
Os arquivos seguem o padrão: `[TIPO]_[DESCRIÇÃO]_[DATA].png`

**Exemplos:**
- `BUG001_lista_vazia_20260309.png` - Screenshot do bug da lista vazia
- `CT001_cadastro_sucesso_20260309.png` - Evidência do caso de teste CT001
- `FLOW_cadastro_completo_20260309.png` - Fluxo completo de cadastro

### Tipos de Screenshot

#### 🐛 Bugs (BUG)
- Capturas de tela demonstrando bugs identificados
- Include contexto completo da tela
- Formato: `BUG[ID]_[descrição]_[data].png`

#### 🧪 Casos de Teste (CT)
- Evidências de execução dos casos de teste
- Resultados esperados vs obtidos
- Formato: `CT[ID]_[descrição]_[data].png`

#### 🔄 Fluxos (FLOW)
- Capturas de fluxos completos da aplicação
- Navegação entre telas
- Formato: `FLOW_[descrição]_[data].png`

#### ✅ Validações (VAL)
- Screenshots de mensagens de validação
- Tratamento de erros
- Formato: `VAL_[descrição]_[data].png`

#### 📱 Responsividade (RESP)
- Testes em diferentes resoluções
- Comportamento mobile/desktop
- Formato: `RESP_[resolução]_[data].png`

## 📋 Lista de Screenshots Planejados

### Bugs Identificados
- [ ] `BUG001_lista_vazia_20260309.png` - Lista sem mensagem informativa

### Casos de Teste Principais
- [ ] `CT001_cadastro_valido_20260309.png` - Cadastro com dados válidos
- [ ] `CT002_validacao_nome_20260309.png` - Validação campo nome obrigatório
- [ ] `CT003_validacao_descricao_20260309.png` - Validação campo descrição
- [ ] `CT004_validacao_carga_20260309.png` - Validação carga horária
- [ ] `CT011_lista_vazia_20260309.png` - Visualização lista vazia
- [ ] `CT012_lista_preenchida_20260309.png` - Lista com cursos cadastrados

### Fluxos Principais
- [ ] `FLOW_tela_inicial_20260309.png` - Tela inicial da aplicação
- [ ] `FLOW_formulario_cadastro_20260309.png` - Formulário de cadastro
- [ ] `FLOW_lista_cursos_20260309.png` - Tela de listagem de cursos
- [ ] `FLOW_navegacao_completa_20260309.png` - Navegação entre telas

### Validações
- [ ] `VAL_campo_obrigatorio_20260309.png` - Mensagens de campo obrigatório
- [ ] `VAL_formato_invalido_20260309.png` - Validação de formato
- [ ] `VAL_sucesso_cadastro_20260309.png` - Mensagem de sucesso

## 🎯 Diretrizes para Captura

### Qualidade
- Resolução mínima: 1280x720
- Formato: PNG (melhor qualidade)
- Capturar tela completa quando relevante
- Focar no elemento específico quando necessário

### Contexto
- Incluir navegador e URL quando relevante
- Mostrar mensagens de erro/sucesso completas
- Capturar estado antes e depois de ações
- Incluir timestamp quando importante

### Organização
- Nomear arquivos de forma descritiva
- Incluir data da captura
- Agrupar por tipo de evidência
- Referenciar nos relatórios de teste

## 📝 Como Usar

1. **Durante execução de testes:** Capturar screenshots de cada etapa importante
2. **Ao encontrar bugs:** Documentar com screenshot completo do problema
3. **Para validações:** Capturar mensagens e comportamentos
4. **Em fluxos:** Documentar navegação completa entre telas

## 🔗 Referências

Todas as screenshots são referenciadas em:
- [Casos de Teste](../../test-cases/test-cases-link.md)
- [Relatório de Bugs](../../bug-reports/bugs.md)
- [Análise da Aplicação](../../docs/application-analysis.md)

---

**Status:** 📸 Pronto para coleta de evidências
**Última atualização:** 9 de março de 2026

*As capturas de tela serão adicionadas conforme a execução dos testes progride.*