+++
title = 'Cyberpouvoirs'
date = 2023-03-24T00:16:51+02:00
draft = true
+++

# Introduction

Le vocabulaire de la cryptographie étant souvent complexe, il me semble interessant de réfléchir à des images plus parlantes à des fins de vulgarisation.

Une adresse réfère à un moyen de créer un canal sécurisé, tandis qu'identité réfère à un moyen de l'identifier.

La cryptographie garantie les cyberpouvoirs par des modèles mathématiques plutôt que via des platformes ou via l'infrastructure du réseau.

# Identité numérique

*Propriétés: Confidentialité et Integrité*

À des fins de vulgarisation au lieu de "clé publique de signature électronique" nous diront simplement "identité numérique".
Nous nous référons à un grand nombre qui permet de vérifier les signatures numériques générés par un autre grand nombre qui lui est associé (appelé "clé privée" ou "clé secrète").

Afin de différencier ce qu'on appelle identité numérique des autres formes d'identités numériques, nous l'appelleront "identité numérique cryptographique" lorsque la distinction est nécessaire.

La connaissance de la clé secrète est l'unique moyen de générer une signature au nom de cette identité numérique.
Toute personne peut vérifier la signature d'un utilisateur par simple connaissance de son identité numérique, ce qui est forme un mécanisme d'authentification sans intermédiaire, décentralisée.


# Adresse numérique

*Propriétés: Authentification*

À des fins de vulgarisation au lieu de "clé publique de chiffrement asymétrique" nous diront simplement "adresse numérique".
Nous nous référons à un grand nombre qui permet de sceller une enveloppe que seul le possesseur d'un autre grand nombre (appelé "clé privée" ou "clé secrète") pourra ouvrir.

Afin de différencier ce qu'on adresse numérique des autres formes d'adresses numériques, nous l'appelleront "adresse numérique cryptographique" lorsque la distinction est nécessaire.

Toute personne peut envoyer un message uniquement destiné à un utilisateur par simple connaissance de son adresse numérique, peu importe les intermédiaires. On dit alors que le message est chiffré de bout-en-bout.
La connaissance de la clé secrète de l'adresse numérique est le seul moyen de décrypter ce message.
