# Utilise la même image de base pour rester cohérent
FROM node:22-alpine

# Définit le répertoire de travail
WORKDIR /app

# Copie les fichiers de dépendances
COPY package*.json ./

# Installe les dépendances
RUN npm install

# Copie le code source du frontend
COPY . .

# Commande pour lancer le serveur de développement
CMD ["npm", "run", "dev"]