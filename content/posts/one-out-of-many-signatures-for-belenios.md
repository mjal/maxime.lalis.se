+++
title = 'One Out of Many Signatures for Belenios'
date = 2024-10-21T21:02:47+02:00
+++

[Cet article](https://eprint.iacr.org/2014/764) propose un "zerocoin scheme": c'est à dire un protocole de ring-signature, où chaque possesseur d'un jeton doit dévoiler une valeur _serial_ en même temps que sa signature. Chaque _serial_ **bound** son utilisateur à un jeton de signature sans dévoiler lequel.

J'ai donc fait [un brouillon d'implémentation possible](/belenios-ooom.pdf) dans Belenios (en copiant beaucoup les documents existants...). Intuitivement, cela me semble fonctionner, mais je m'en suis pas sûr.

Ce système utilise deux secrets: `s` et `serial` (qui pourraient être dérivé de la même seed). Le revote corresponds alors à la réutilisation du même `serial`.

L'implémentation naive que je propose est couteuse, chaque signature a une complexité linéaire en fonction du nombre de jetons possibles. L'article propose une solution en complexité logarithmique qui me dépasse encore. J'ai aussi trouvé [une implémentation](https://github.com/cloudflare/zkp-ecdsa/blob/main/src/proofGK/gk.ts) par cloudflare, avec l'optimisation.
