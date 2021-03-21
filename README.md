# TLC_TP

# Kévin MARQUER

Ce readme décris du mieux que je peux la partie TP de TLC du au fait que cela fait un long momment
depuis la réalisation de ces exercices.

## Partie 1: #

La première partie concerne la réalisation d'un docker compose pour déployer votre vos 4 services nginx et votre loadbalancer.
Loadbalancer est le service tlc-proxy suivie de quatre services nginx tlcl identique avec un numéro qui les différencies.








## Partie 2 #

Création d'un docker file pour lancé une application.

Erreur lors du lancement du docker build, il ne reconnait pas l'instruction "java" dans CMD l'erreur est juste un espace qui manque entre CMD et le crochet.
Ensuite quand je lance le docker build j'obtient à la fin :
```
Do you want to continue? [Y/n] Abort.
The command '/bin/sh -c apt-get install git' returned a non-zero code: 1
```
Cela viens d'une erreur dans les apt-get. J'ai donc remis par rapport à ceux du readme de l'appli.
Ensuite j'obtient une nouvelle erreurs.
```
E: Unable to locate package libjasper1
The command '/bin/sh -c apt-get update  && apt-get install -y openjdk-8-jdk && apt-get install -y maven && apt-get install -f libpng16-16 && apt-get install -f libjasper1 && get install -f libdc1394-22 && apt-get install git' returned a non-zero code: 100
```

Je choisi de retirer le apt-get libjasper1, voici ce que j'obtient ensuite :
```
/bin/sh: 1: get: not found
The command '/bin/sh -c apt-get update  && apt-get install -y openjdk-8-jdk && apt-get install -y maven && apt-get install -f libpng16-16 && get install -f libdc1394-22 && apt-get install git' returned a non-zero code: 127
```

