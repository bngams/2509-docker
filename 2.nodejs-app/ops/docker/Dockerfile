FROM node:22.19-alpine3.22

WORKDIR /app

# Cache optimization
# J'installe les dépendances avant de copier le reste des fichiers
# Je limite l'imapct des modifs sur le code / projet...
COPY package.json .
RUN npm install

COPY . .

CMD ["node", "src/index.js"]


