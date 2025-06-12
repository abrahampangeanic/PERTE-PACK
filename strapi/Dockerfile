# Usa una imagen base de Node.js 20
FROM node:20-alpine

# Instalar herramientas necesarias
RUN apk add --no-cache git openssl

# Define el directorio de trabajo
WORKDIR /app

ARG GITHUB_TOKEN
RUN git clone https://$GITHUB_TOKEN@github.com/Pangeamt/PERTE-STRAPI.git .

# # Clona el repositorio directamente de la rama main
# RUN git clone --branch main https://github.com/Pangeamt/PERTE-STRAPI.git .

# Copia el archivo .env
COPY .env ./

# Instala pnpm globalmente
RUN npm install 

# Construye el proyecto Next.js
RUN npm run build

# Expone el puerto
EXPOSE 1337

# Inicia la aplicación Next.js
CMD ["npm", "run", "start"]