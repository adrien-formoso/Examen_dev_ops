# Utilise l'image Node.js 22 basée sur Alpine Linux (plus légère)
FROM node:22-alpine

# Définit le répertoire de travail dans le conteneur
WORKDIR /app

# Copie les fichiers de configuration des dépendances en premier
# (Cela permet de mettre en cache l'étape npm install si le code change mais pas les dépendances)
COPY package*.json ./

# Installe les dépendances
RUN npm install

# Copie le reste des fichiers du projet
COPY . .

# Expose le port 3000 pour la communication avec l'extérieur
EXPOSE 3000

# Commande par défaut pour lancer l'application
CMD ["node", "index.js"]