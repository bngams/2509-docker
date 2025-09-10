FROM python:3.13.7-alpine3.21

# comme le répertoire HOME
# toutes les instructions suivantes seront exécutées dans ce répertoire
WORKDIR /app

# COPY SRC DESTINATION
# COPY . => le point signifie le répertoire courant (prise en compte du .dockerignore)
# . => dossier destination dans le container (dossier en cours = /app spécifié par WORKDIR)
COPY . .

# RUN => exécuter une commande dans le container "temporaire" (pour préparer l'image finale)
RUN pip install --no-cache-dir -r requirements.txt

# CMD => commande par défaut lorsque le container sera démarré
CMD ["python", "index.py"]