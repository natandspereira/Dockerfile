# Coleção de Dockerfiles
Este repositório contém uma coleção de **Dockerfiles** para diferentes serviços e aplicações. O objetivo é fornecer imagens de contêiner configuráveis e reutilizáveis, prontas para facilitar o desenvolvimento, testes e deploy de aplicações em ambientes isolados.

### 📂 Estrutura do repositório
- Dockerfile.* — Arquivos Dockerfile individuais para diferentes serviços ou propósitos.
- Cada Dockerfile é independente e pode ser construído e executado separadamente.  

### 🚀 Como usar
- docker run -d -p PORTA_LOCAL:PORTA_CONTAINER minha-imagem:latest (background) <br>
- docker run -it -p PORTA_LOCAL:PORTA_CONTAINER minha-imagem:latest /bin/bash <br>
Substitua PORTA_LOCAL e PORTA_CONTAINER conforme necessidade do seu projeto.

### Build da imagem
docker build -f Dockerfile.exemplo -t minha-imagem:v1.0 .

### 🔧 Boas práticas
- Use tags específicas para imagens base, evitando latest.
- Minimize o número de camadas no Dockerfile para otimizar o build.
- Configure permissões adequadas aos arquivos e evite rodar como root quando possível.
- Utilize .dockerignore para evitar incluir arquivos desnecessários na imagem.
