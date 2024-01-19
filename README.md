<!-- markdownlint-disable MD030 -->

# AI-CRISP

[![Notas de Lançamento](https://img.shields.io/github/release/FlowiseAI/Flowise)](https://github.com/FlowiseAI/Flowise/releases)
[![Discord](https://img.shields.io/discord/1087698854775881778?label=Discord&logo=discord)](https://discord.gg/jbaHfsRVBW)
[![Twitter Follow](https://img.shields.io/twitter/follow/FlowiseAI?style=social)](https://twitter.com/FlowiseAI)
[![Gráfico de estrelas do GitHub](https://img.shields.io/github/stars/FlowiseAI/Flowise?style=social)](https://star-history.com/#FlowiseAI/Flowise)
[![GitHub fork](https://img.shields.io/github/forks/FlowiseAI/Flowise?style=social)](https://github.com/FlowiseAI/Flowise/fork)

<h3>Arraste e solte a interface do usuário para construir seu fluxo LLM personalizado</h3>
<a href="https://github.com/FlowiseAI/Flowise">
<img width="100%" src="https://github.com/FlowiseAI/Flowise/blob/main/images/flowise.gif?raw=true"></a>

## ⚡Início Rápido

Baixe e instale [NodeJS](https://nodejs.org/en/download) >= 18.15.0

1. Instale o Flowise
    ```bash
    npm install -g flowise
    ```
2. Inicie o Flowise

    ```bash
    npx flowise start
    ```

    Com nome de usuário e senha

    ```bash
    npx flowise start --FLOWISE_USERNAME=user --FLOWISE_PASSWORD=1234
    ```

3. Abra [http://localhost:3000](http://localhost:3000)

## 🐳 Docker

### Docker Compose

1. Vá para a pasta `docker` na raiz do projeto
2. Copie o arquivo `.env.example`, cole-o no mesmo local e renomeie para `.env`
3. `docker-compose up -d`
4. Abra [http://localhost:3000](http://localhost:3000)
5. Você pode parar os contêineres com `docker-compose stop`

### Imagem Docker

1. Construa a imagem localmente:
    ```bash
    docker build --no-cache -t flowise .
    ```
2. Execute a imagem:

    ```bash
    docker run -d --name flowise -p 3000:3000 flowise
    ```

3. Pare a imagem:
    ```bash
    docker stop flowise
    ```

## 👨‍💻 Desenvolvedores

Flowise possui 3 módulos diferentes em um único repositório mono.

-   `server`: Backend Node para servir lógicas de API
-   `ui`: Frontend React
-   `components`: Componentes Langchain

### Pré-requisitos

-   Instale o [Yarn v1](https://classic.yarnpkg.com/en/docs/install)
    ```bash
    npm i -g yarn
    ```

### Configuração

1. Clone o repositório

    ```bash
    git clone https://github.com/FlowiseAI/Flowise.git
    ```

2. Vá para a pasta do repositório

    ```bash
    cd Flowise
    ```

3. Instale todas as dependências de todos os módulos:

    ```bash
    yarn install
    ```

4. Compile todo o código:

    ```bash
    yarn build
    ```

5. Inicie o aplicativo:

    ```bash
    yarn start
    ```

    Agora você pode acessar o aplicativo em [http://localhost:3000](http://localhost:3000)

6. Para compilação de desenvolvimento:

    - Crie um arquivo `.env` e especifique a `PORTA` (consulte `.env.example`) em `packages/ui`
    - Crie um arquivo `.env` e especifique a `PORTA` (consulte `.env.example`) em `packages/server`
    - Execute

        ```bash
        yarn dev
        ```

    Qualquer alteração de código recarregará o aplicativo automaticamente em [http://localhost:8080](http://localhost:8080)

## 🔒 Autenticação

Para habilitar a autenticação no nível do aplicativo, adicione `FLOWISE_USERNAME` e `FLOWISE_PASSWORD` ao arquivo `.env` em `packages/server`:

FLOWISE_USERNAME=user
FLOWISE_PASSWORD=1234


## 🌱 Variáveis de Ambiente

Flowise suporta diferentes variáveis de ambiente para configurar sua instância. Você pode especificar as seguintes variáveis no arquivo `.env` dentro da pasta `packages/server`. Leia [mais](https://github.com/FlowiseAI/Flowise/blob/main/CONTRIBUTING.md#-env-variables)

## 📖 Documentação

[Documentação do Flowise](https://docs.flowiseai.com/)

## 🌐 Auto-hospedagem

Implante o Flowise auto-hospedado em sua infraestrutura existente, suportamos várias [implantações](https://docs.flowiseai.com/configuration/deployment)

-   [AWS](https://docs.flowiseai.com/deployment/aws)
-   [Azure](https://docs.flowiseai.com/deployment/azure)
-   [Digital Ocean](https://docs.flowiseai.com/deployment/digital-ocean)
-   [GCP](https://docs.flowiseai.com/deployment/gcp)
-   <details>
      <summary>Outros</summary>

    -   [Railway](https://docs.flowiseai.com/deployment/railway)

        [![Implantar no Railway](https://railway.app/button.svg)](https://railway.app/template/pn4G8S?referralCode=WVNPD9)

    -   [Render](https://docs.flowiseai.com/deployment/render)

        [![Implantar no Render](https://render.com/images/deploy-to-render-button.svg)](https://docs.flowiseai.com/deployment/render)

    -   [HuggingFace Spaces](https://docs.flowiseai.com/deployment/hugging-face)

        <a href="https://huggingface.co/spaces/FlowiseAI/Flowise"><img src="https://huggingface.co/datasets/huggingface/badges/raw/main/open-in-hf-spaces-sm.svg" alt="HuggingFace Spaces"></a>

    -   [Elestio](https://elest.io/open-source/flowiseai)

        [![Implantar](https://pub-da36157c854648669813f3f76c526c2b.r2.dev/deploy-on-elestio-black.png)](https://elest.io/open-source/flowiseai)

    -   [Sealos](https://cloud.sealos.io/?openapp=system-template%3FtemplateName%3Dflowise)

        [![](https://raw.githubusercontent.com/labring-actions/templates/main/Deploy-on-Sealos.svg)](https://cloud.sealos.io/?openapp=system-template%3FtemplateName%3Dflowise)

    -   [RepoCloud](https://repocloud.io/details/?app_id=29)

        [![Implantar no RepoCloud](https://d16t0pc4846x52.cloudfront.net/deploy.png)](https://repocloud.io/details/?app_id=29)

      </details>

## 📄 Licença

O código fonte neste repositório está disponível sob a [Licença Apache Versão 2.0](LICENSE.md).
