# CEP Autofill for Oracle

## Descrição curta
Preenche automaticamente endereços a partir do CEP brasileiro em sites Oracle, com suporte a múltiplas APIs e fallback inteligente.

## Descrição completa
O CEP Autofill for Oracle é uma extensão que simplifica o preenchimento de formulários em sites Oracle. Quando você digita um CEP brasileiro em qualquer formulário do site https://acc2-oc.oracleindustry.com/, a extensão busca automaticamente as informações de endereço e preenche os campos correspondentes.

### Principais recursos:

✓ **Detecção automática** de campos de CEP em formulários
✓ **Preenchimento automático** de campos de endereço (logradouro, bairro, cidade, estado)
✓ **Sistema multi-API com fallback** que utiliza até 4 provedores diferentes para garantir alta disponibilidade
✓ **Consulta manual** de CEPs através do popup da extensão
✓ **Monitor de status** que mostra quais APIs estão operacionais
✓ **Configurações personalizáveis** para adequar o comportamento às suas necessidades
✓ **Requisitos mínimos de permissão** para garantir sua privacidade e segurança

### Como usar:

1. Instale a extensão e acesse qualquer página em https://acc2-oc.oracleindustry.com/
2. Digite um CEP válido em qualquer campo de CEP/código postal
3. A extensão detectará automaticamente o campo e preencherá o endereço quando você sair do campo
4. Você também pode realizar consultas manuais clicando no ícone da extensão

### Segurança e privacidade:

- A extensão atua apenas no domínio especificado (https://acc2-oc.oracleindustry.com/)
- Não coleta, armazena ou compartilha dados pessoais
- Utiliza apenas as permissões mínimas necessárias (storage, activeTab)
- Implementa Content Security Policy para garantir segurança adicional

### Provedores de CEP suportados:

1. ViaCEP (primário)
2. BrasilAPI (primeira alternativa)
3. ApiCEP (segunda alternativa)
4. OpenCEP (terceira alternativa)

Se uma API estiver indisponível, a extensão tentará automaticamente a próxima, garantindo o funcionamento mesmo quando um serviço estiver fora do ar.

### Requisitos:

- Funciona apenas em https://acc2-oc.oracleindustry.com/
- Requer conexão com internet para consultar as APIs de CEP
- Compatível com Google Chrome 88+

Simplifique o preenchimento de endereços em sistemas Oracle e economize tempo com o CEP Autofill!

## Categoria
Produtividade

## Idiomas suportados
Português (Brasil)

## Tags
cep, brasil, endereço, formulário, oracle, autopreenchimento, automação