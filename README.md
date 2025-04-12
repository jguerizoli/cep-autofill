# CEP Autofill for Oracle - Documentação

## Visão Geral

A extensão CEP Autofill for Oracle é uma ferramenta que simplifica o preenchimento de formulários em sites Oracle, automatizando a busca e preenchimento de endereços brasileiros a partir do CEP (Código de Endereçamento Postal).

## Funcionalidades Principais

- **Detecção Automática de Campos**: Identifica campos de CEP em formulários automaticamente
- **Preenchimento Automático**: Preenche os campos de endereço (logradouro, bairro, cidade, estado) quando um CEP é digitado
- **Sistema Multi-API com Fallback**: Utiliza múltiplas APIs de CEP com mecanismo de fallback para garantir alta disponibilidade 
- **Consulta Manual**: Permite consultar CEPs manualmente através do popup da extensão
- **Monitor de Status de Serviços**: Informa quais provedores de CEP estão online ou offline
- **Configurações Personalizáveis**: Permite ativar/desativar a detecção automática e o preenchimento automático

## Instalação

1. Baixe a extensão da Chrome Web Store
2. Clique no ícone da extensão na barra de ferramentas
3. Configure as opções conforme necessário (auto-detecção e auto-preenchimento vêm ativados por padrão)

## Como Usar

### Preenchimento Automático
1. Navegue até qualquer página em https://acc2-oc.oracleindustry.com/
2. Preencha um campo de CEP válido
3. Quando você sair do campo (evento "blur"), a extensão buscará automaticamente o endereço
4. Os campos de endereço serão preenchidos automaticamente se encontrados

### Consulta Manual
1. Clique no ícone da extensão na barra de ferramentas para abrir o popup
2. Digite um CEP válido no campo de consulta manual
3. Clique em "Consultar"
4. A extensão preencherá os campos de endereço na página atual, se disponíveis

### Verificar Status dos Serviços
1. Abra o popup da extensão
2. Veja a seção "Status dos Serviços" para verificar quais APIs estão funcionando
3. Clique no botão de atualização para verificar novamente

## APIs Suportadas

A extensão utiliza as seguintes APIs de CEP, na ordem de prioridade:

1. **ViaCEP** (primária) - https://viacep.com.br/
2. **BrasilAPI** (primeira alternativa) - https://brasilapi.com.br/
3. **ApiCEP** (segunda alternativa) - https://apicep.com/
4. **OpenCEP** (terceira alternativa) - https://opencep.com/

Se uma API estiver indisponível ou retornar erro, a extensão tentará a próxima na sequência automaticamente.

## Resolução de Problemas

### Endereço não é preenchido automaticamente
- Verifique se todas as APIs estão offline na seção de status
- Confirme se o CEP digitado está correto
- Verifique se os campos de endereço existem na página e seguem os padrões de nomenclatura comuns
- Certifique-se de que as configurações de auto-detecção e auto-preenchimento estão ativadas

### A extensão não carrega
- Atualize a página
- Reinstale a extensão
- Verifique se o domínio está correto (apenas funciona em acc2-oc.oracleindustry.com)

## Privacidade e Segurança

A extensão:
- Não armazena ou transmite os endereços consultados para servidores externos
- Não coleta dados de navegação ou quaisquer informações pessoais
- Usa apenas permissões mínimas necessárias (storage, activeTab)
- Implementa Content Security Policy para maior segurança

Para mais detalhes, consulte nossa [Política de Privacidade](PRIVACY_POLICY.md).

## Código Fonte

O código fonte completo desta extensão está disponível em [GitHub](https://github.com/cep-autofill-extension) sob licença MIT.