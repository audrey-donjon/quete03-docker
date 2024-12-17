# Image basé sur Node.js lts
FROM node:lts-alpine

# Création du répertoire de l'application
RUN mkdir /app
WORKDIR /app

# Installation des dépendances
COPY package*.json ./
RUN npm i

# Copie des fichiers source
COPY src src

# Exposition du port utilisé par l'application
EXPOSE 5000

# Définition de la commande pour démarrer l'application
CMD ["npm", "start"]