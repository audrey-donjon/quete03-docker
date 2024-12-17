# Image basé sur Node.js lts
FROM node:lts-alpine

# Création du répertoire de l'application
RUN mkdir /app
WORKDIR /app

# Installation des dépendances
COPY package*.json ./
RUN npm i

# Copie des fichiers source
COPY vite.config.js vite.config.js
COPY index.html index.html
COPY public ./public
COPY src src

# Build de l'application React
RUN npm run build

# Exposition du port utilisé par l'application
EXPOSE 8080

# Définition de la commande pour démarrer l'application
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0", "--port", "8080"]