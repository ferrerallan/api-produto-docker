
# API Product with MongoDB and Docker

## Description

This repository demonstrates how to set up a product API using MongoDB and Docker. It includes the necessary configuration files and instructions to build and run the application in a Docker container.

## Requirements

- Docker
- Node.js 12+

## Mode of Use

1. Clone the repository:
   ```bash
   git clone https://github.com/ferrerallan/api-produto-docker.git
   ```
2. Navigate to the project directory:
   ```bash
   cd api-produto-docker
   ```
3. Build the Docker image:
   ```bash
   docker build -t api-produto .
   ```
4. Run the Docker container:
   ```bash
   docker run -p 3000:3000 api-produto
   ```

## Use Case

This repository can be used as a reference for deploying a Node.js application with MongoDB using Docker. It is particularly useful for:

- Rapid development and testing of APIs
- Learning how to containerize Node.js applications
- Creating scalable and portable application environments

## Example of Use

### Dockerfile

The `Dockerfile` sets up the Node.js environment and installs dependencies:

```dockerfile
FROM node:12
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD ["node", "src/index.js"]
```

### Running the Application

After building the Docker image, run the container to start the application:

```bash
docker build -t api-produto .
docker run -p 3000:3000 api-produto
```

## License

This project is licensed under the MIT License.
