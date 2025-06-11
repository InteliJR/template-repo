# 📚 Configuração da Documentação

Este diretório contém a documentação do projeto utilizando [Docusaurus](https://docusaurus.io/).

## Configuração Inicial

Para configurar a documentação em um novo repositório, siga os passos abaixo:

1. **Configuração do GitHub Pages**:
   - Vá para as configurações do repositório (Settings)
   - Na seção "Pages", selecione a branch `gh-pages` como source
   - Selecione a pasta `/ (root)` como diretório

2. **Configuração do Docusaurus**:
   - Abra o arquivo `docs/docusaurus.config.ts`
   - Atualize os seguintes campos:
     - `title`: Nome do seu projeto
     - `tagline`: Descrição do seu projeto
     - `url`: Deve ser "https://[nome-da-organizacao].github.io"
     - `baseUrl`: Deve ser "/[nome-do-repositorio]/"
     - `organizationName`: Nome da sua organização no GitHub
     - `projectName`: Nome do seu repositório

## Desenvolvimento Local

```bash
# Acesse o diretório docs
cd docs

# Instale as dependências
npm install

# Inicie o servidor de desenvolvimento
npm start
```

## Deploy

### Deploy Automático
O deploy automático acontece sempre que há um push na branch `main`. O GitHub Action configurado irá buildar e publicar a documentação automaticamente. Se isso não acontecer, é necessário verificar se houve algum erro na pipeline.

### Deploy Manual (se necessário)
```bash
# No diretório docs
npm run deploy
```

## Estrutura do Diretório

```
docs/
├── docs/                 # Arquivos de documentação em Markdown
├── src/                  # Arquivos fonte do site
├── static/              # Arquivos estáticos (imagens, etc)
├── docusaurus.config.ts # Configuração principal
├── package.json         # Dependências e scripts
└── README.md            # Este arquivo
``` 