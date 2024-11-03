+++
title = 'Protocole Bitmessage'
date = 2024-10-03T12:53:27+02:00
+++

[Bitmessage](https://en.wikipedia.org/wiki/Bitmessage) est un logiciel de messagerie sans métadonnées.

Le protocole est simple, à défaut d'être scalable. Il est uniquement basé sur le chiffrement symétrique.
- Les clés de chiffrement sont transmises via d'autres canaux.
- Les messages chiffrés sont envoyés sur une base de données distribuée.
- Pour chaque nouveau message sur le réseau réseau, je test toutes mes clés.
- Si je peux le déchiffrer, alors il m'est destiné.

C’est un processus très peu efficace (surtout lorsqu’il y a beaucoup de messages ou qu’on a beaucoup de clés à essayer).

En pratique, il existe des mécanismes pour éviter de saturer le réseau (une proof-of-work associée à chaque message), ce qui le rend tout de même utilisable.

Il présente cependant un grand avantage : réduire au minimum (et très simplement) les métadonnées, comme les informations de source et de destination.

![schema de bitmessage](/bitmessage.jpg)

Je me pose néanmoins la question de la scalabilité de ce genre de protocoles (Peut-on faire mieux que de devoir vérifier tous les messages ?)

Cela ressemble à un problème de [Private Information Retrieval](https://en.wikipedia.org/wiki/Private_information_retrieval): pouvoir requêter le sous-ensemble de message qui me sont destinés sans avoir à dévoiler mon identité. Il ne faut pas être trop spécifique pour garder un _anonimity set_ suffisant. Reste à trouver la bonne primitive pour cette tache (pourquoi pas une sorte de bloom filters ?).
