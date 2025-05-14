<!-- markdownlint-disable MD030 -->

<p align="center">
<img src="https://github.com/saifpashaTrigent/Trigent-AI-Studio-Flowise/blob/main/images/flowise_white.svg#gh-light-mode-only">
<img src="https://github.com/saifpashaTrigent/Trigent-AI-Studio-Flowise/blob/main/images/flowise_dark.svg#gh-dark-mode-only">
</p>


[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://in.linkedin.com/company/trigent-software)
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@trigent-software)
[![X](https://img.shields.io/badge/Trigent-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/TrigentSoftware)



<h3>Visually build your customized LLM flow using Trigent AI Studio’s drag & drop interface—create powerful AI agents with ease.</h3>
<a href="https://github.com/saifpashaTrigent/Trigent-AI-Studio-Flowise">
<img width="100%" src="https://github.com/saifpashaTrigent/Trigent-AI-Studio-Flowise/blob/main/images/flowise_agentflow.gif?raw=true"></a>

## ⚡Quick Start

Download and Install [NodeJS](https://nodejs.org/en/download) >= 18.15.0

1. Install AI Studio
    ```bash
    npm install -g flowise
    ```
2. Start AI Studio

    ```bash
    npx flowise start
    ```

    With username & password

    ```bash
    npx flowise start --FLOWISE_USERNAME=user --FLOWISE_PASSWORD=1234
    ```

3. Open [http://localhost:3000](http://localhost:3000)

## 🐳 Docker

### Docker Compose

1. Clone the AI Studio project
2. Go to `docker` folder at the root of the project
3. Copy `.env.example` file, paste it into the same location, and rename to `.env` file
4. `docker compose up -d`
5. Open [http://localhost:3000](http://localhost:3000)
6. You can bring the containers down by `docker compose stop`

### Docker Image

1. Build the image locally:
    ```bash
    docker build --no-cache -t flowise .
    ```
2. Run image:

    ```bash
    docker run -d --name flowise -p 3000:3000 flowise
    ```

3. Stop image:
    ```bash
    docker stop flowise
    ```

## 👨‍💻 Developers

AI Studio has 3 different modules in a single mono repository.

-   `server`: Node backend to serve API logics
-   `ui`: React frontend
-   `components`: Third-party nodes integrations
-   `api-documentation`: Auto-generated swagger-ui API docs from express

### Prerequisite

-   Install [PNPM](https://pnpm.io/installation)
    ```bash
    npm i -g pnpm
    ```

### Setup

1.  Clone the repository

    ```bash
    git clone https://github.com/FlowiseAI/Flowise.git
    ```

2.  Go into repository folder

    ```bash
    cd Flowise
    ```

3.  Install all dependencies of all modules:

    ```bash
    pnpm install
    ```

4.  Build all the code:

    ```bash
    pnpm build
    ```

    <details>
    <summary>Exit code 134 (JavaScript heap out of memory)</summary>  
      If you get this error when running the above `build` script, try increasing the Node.js heap size and run the script again:

        export NODE_OPTIONS="--max-old-space-size=4096"
        pnpm build

    </details>

5.  Start the app:

    ```bash
    pnpm start
    ```

    You can now access the app on [http://localhost:3000](http://localhost:3000)

6.  For development build:

    -   Create `.env` file and specify the `VITE_PORT` (refer to `.env.example`) in `packages/ui`
    -   Create `.env` file and specify the `PORT` (refer to `.env.example`) in `packages/server`
    -   Run

        ```bash
        pnpm dev
        ```

    Any code changes will reload the app automatically on [http://localhost:8080](http://localhost:8080)

## 🔒 Authentication

To enable app level authentication, add `FLOWISE_USERNAME` and `FLOWISE_PASSWORD` to the `.env` file in `packages/server`:

```
FLOWISE_USERNAME=user
FLOWISE_PASSWORD=1234
```

## 🌱 Env Variables

AI Studio support different environment variables to configure your instance. You can specify the following variables in the `.env` file inside `packages/server` folder. Read [more](https://github.com/FlowiseAI/Flowise/blob/main/CONTRIBUTING.md#-env-variables)

## 📖 Documentation

[AI Studio Docs](https://docs.flowiseai.com/)



