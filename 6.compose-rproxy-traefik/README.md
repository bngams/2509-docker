# Lancer les containers

1. Utiliser l'option compose -f

```
docker compose -f app1/compose.yml -f app2/compose.yml -f traefik/compose.yml up
```

2. Utiliser un fichier .env a la racine qui rassemble tous les fichiers compose:

```
COMPOSE_FILE=app1/compose.yml:app2/compose.yml:traefik/compose.yml
COMPOSE_PROJECT_NAME=myproject   # optional, neatens container names
```

Et comme ceci on a accès à tout avec les éléments avec les commandes classiques...


3. Script personnalisé...

