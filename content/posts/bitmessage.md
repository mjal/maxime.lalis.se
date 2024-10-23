+++
title = 'Bitmessage'
date = 2024-10-03T12:53:27+02:00
+++

[Bitmessage](https://en.wikipedia.org/wiki/Bitmessage) est un logiciel de messagerie minimisant les métadonnées.

Le protocole est simple, à défaut d'être scalable.
- Les clés (symétriques) de chiffrement sont transmises sur d'autres canaux.
- Les messages sont chiffrés et envoyés sur une base de donnée distribuée.
- Pour chaque nouveau message du réseau, j'essaye toutes mes clés.
- Si une clé de chiffrement fonctionne, alors c'est un message pour cette conversation.

C'est un processus très peu efficace, mais qui a un avantage : réduire à leur minimum les métadonnées, comme les informations de source et destination.

![schema de bitmessage](/bitmessage.jpg)

En pratique, il y a des mécanisme pour éviter de flooder le réseau (une proof-of-work associé à chaque message).

Je me pose néanmoins la question de la scalabilité de ce genre de protocoles (Peut-on faire mieux que de devoir vérifier tous les messages ?)

Cela ressemble à un problème de [Private Information Retrieval](https://en.wikipedia.org/wiki/Private_information_retrieval): pouvoir requêter le sous-ensemble de message qui me sont destinés sans avoir à dévoiler mon identité. Il ne faut pas être trop spécifique pour garder un _anonimity set_ suffisant. Reste à trouver la bonne primitive pour cette tache (pourquoi pas une sorte de bloom filters ?).
