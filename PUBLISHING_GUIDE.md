# Guia de Publicação na Chrome Web Store

Este guia contém instruções passo a passo para publicar a extensão "CEP Autofill for Oracle" na Chrome Web Store.

## Pré-requisitos

1. Conta de desenvolvedor na Chrome Web Store (taxa única de $5.00 USD)
2. Extensão empacotada em formato .zip
3. Imagens e recursos gráficos necessários
4. Descrições e detalhes da extensão

## Prepare os Recursos Gráficos

Você precisa ter os seguintes recursos gráficos:

- **Ícone da extensão**: Já incluído no pacote nos tamanhos 16x16, 48x48 e 128x128 pixels
- **Ícone da loja**: Imagem de 128x128 pixels para exibição na loja
- **Screenshots**: Entre 1-5 capturas de tela da extensão em uso (1280x800 ou 640x400 pixels)
- **Imagem promocional pequena** (opcional): 440x280 pixels
- **Imagem promocional grande** (opcional): 920x680 pixels
- **Imagem promocional em destaque** (opcional): 1400x560 pixels

## Processo de Publicação

### 1. Crie o arquivo ZIP final

Execute o script de empacotamento para criar o arquivo final:

```bash
node package-for-store.js
```

Isso irá gerar o arquivo `cep-autofill-extension-final.zip` contendo todos os arquivos necessários para a extensão.

### 2. Acesse o Developer Dashboard

1. Acesse [Chrome Web Store Developer Dashboard](https://chrome.google.com/webstore/devconsole)
2. Faça login com sua conta Google de desenvolvedor
3. Clique em "New Item" (Novo item)

### 3. Faça o Upload da Extensão

1. Clique no botão "Upload" e selecione o arquivo `cep-autofill-extension-final.zip`
2. Aguarde o upload e processamento do arquivo

### 4. Preencha as Informações da Loja

Use os arquivos na pasta `store-assets` para preencher os seguintes campos:

#### Detalhes do Item
- **Nome da extensão**: CEP Autofill for Oracle
- **Descrição curta**: Preencha com a primeira linha do arquivo STORE_DESCRIPTION.md
- **Descrição detalhada**: Copie o conteúdo principal do arquivo STORE_DESCRIPTION.md
- **Idioma**: Português (Brasil)
- **Categoria**: Produtividade
- **Faça o upload dos ícones e screenshots** conforme mencionado acima

#### Detalhes da Privacidade
- **Permissões**: Justifique cada permissão usada:
  - `storage`: "Armazenar as configurações do usuário"
  - `activeTab`: "Permitir interação com a página ativa para preencher formulários"
  - `host_permissions`: "Acessar APIs de CEP e site Oracle para funcionalidade principal"
- **Política de Privacidade**: Copie o URL onde você hospedou o arquivo PRIVACY_POLICY.md ou seu conteúdo completo

#### Conteúdo da Extensão
- **Conteúdo da Extensão > Recursos e funcionalidades**: "Preenchimento automático de endereços a partir de CEP brasileiro"
- **Conteúdo da Extensão > Público-alvo do site**: "Usuários do site Oracle Industry Cloud (acc2-oc.oracleindustry.com)"

#### Distribuição e Visibilidade
- **Visibilidade**: Público (listado na Chrome Web Store) ou Privado (apenas com link direto)
- **Países e regiões**: Todos (ou especifique apenas Brasil se preferir)

### 5. Submeta para Revisão

1. Verifique todos os campos e certifique-se de que você forneceu todas as informações necessárias
2. Clique em "Submit for Review" (Enviar para revisão)
3. Aguarde a revisão da Google, que geralmente leva entre 24 horas e 3 dias

## Após a Aprovação

- Sua extensão estará disponível na Chrome Web Store
- Você receberá um e-mail de confirmação
- Você pode compartilhar o link direto para sua extensão na loja ou anunciar por outros meios

## Atualizações Futuras

Para atualizar a extensão:

1. Incremente o número da versão no arquivo `manifest.json`
2. Crie um novo arquivo ZIP seguindo o processo acima
3. Acesse o Developer Dashboard e selecione sua extensão
4. Clique em "Package" e faça o upload da nova versão
5. Submeta para revisão novamente

## Problemas Comuns e Soluções

- **Extensão rejeitada**: Leia com atenção o motivo. Geralmente está relacionado a problemas de permissões, descrição inadequada ou problemas de segurança.
- **Problemas com o ícone**: Certifique-se de que seus ícones estão nos formatos e tamanhos corretos.
- **Descrição inadequada**: Seja claro e específico sobre o que sua extensão faz, sem promessas exageradas.

## Recursos Adicionais

- [Documentação oficial da Chrome Web Store](https://developer.chrome.com/docs/webstore/)
- [Melhores práticas para listagem de extensões](https://developer.chrome.com/docs/webstore/best_practices/)