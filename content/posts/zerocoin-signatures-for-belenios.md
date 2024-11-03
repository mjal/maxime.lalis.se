+++
title = 'Zerocoin signatures for Belenios'
date = 2024-10-21T21:02:47+02:00
+++

[Cet article](https://eprint.iacr.org/2014/764) propose un "zerocoin scheme": c'est à dire un protocole de signature de cercle (ring-signature), dans lequel chaque possesseur d'un jeton doit dévoiler une valeur _serial_ en même temps qu'il signe. Chaque _serial_ lie (bound) son utilisateur à un jeton de signature sans dévoiler lequel (par l'utilisation d'un commitment).

C'est un système qui utilise deux secrets: `s` et `serial` (qui pourraient être dérivé de la même _seed_). Une seconde signature à partir du même jeton réutilise nécessairement le même `serial`.

Voici [un brouillon de spécification](/belenios-zerocoin/belenios-zerocoin.pdf) dans Belenios (en m'inspirant largement des documents existants). Intuitivement, cela me semble fonctionner, mais je m'en suis pas sûr. Il manque une optimisation qui permet de réduire la complexité, mais je préfère d'abord valider cette version simple avant de chercher des optimisations.

[Une implémentation du protocole par cloudflare](https://github.com/cloudflare/zkp-ecdsa/blob/main/src/proofGK/gk.ts).
