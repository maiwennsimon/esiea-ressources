# SUBMISSION

## Step 1 - Prerequis
- Un clone de ce repo GitHub (uniquement si vous n'avez pas accès aux image depuis un registre)
- Installez docker et docker-compose ([ voir la doc ici ](https://docs.docker.com/engine/install/))
- Ayez à votre disposition le registre privé hébergeant les images ou un registre ou vous pourrez les sauvegarder

## Step 2 - Construction des images (no need for deployment only)
#### UNIQUEMENT SI VOUS AVEZ BESION SINON UTILISER LES IMAGES DU REGISTRE PRIVE
- Lancez la commande ```docker-compose -f docker-compose.yml build```
       - Modifiez le fichier "docker-compose.yml" si vous voulez spécifier un autre registre

## Step 3 - Déploiement depuis le registre
- Si vous avez reconstruit les conteneurs sur un autre registre privé :
       - Modifiez le fichier "compose.yml" pour spécifier votre registre
- Lancez la commande ```docker-compose -f compose.yml up -d```
- Vous pouvez verifiez que tout est bien demmarré avec la commande ```docker-compose logs -f```
       - Vous devriez obtenir une sortie de ce genre :

![logs](https://media.discordapp.net/attachments/1119205825039314976/1193506694412652636/docker-compose_logs.png?ex=65acf6ba&is=659a81ba&hm=206a4423d52992665f1dca87ffc8e2400463e8df773e19510bd3b70f707d91b5&=&format=webp&quality=lossless&width=726&height=670)

- Vous pouvez également verifiez que tous les conteneurs sont "healthy" avec ```docker ps```
       - Vous devriez obtenir une sortie de ce genre :

![docker_ps](https://media.discordapp.net/attachments/1119205825039314976/1193513622622716055/docker_ps_private_registery.png?ex=65acfd2e&is=659a882e&hm=0d569d348efb98a26189b01b557a99e7db191eaa217f686fc9eb39447cac0ed1&=&format=webp&quality=lossless&width=1439&height=97)
