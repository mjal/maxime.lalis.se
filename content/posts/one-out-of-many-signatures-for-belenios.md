+++
title = 'One Out of Many Signatures for Belenios'
date = 2024-10-21T21:02:47+02:00
+++

Étant passionné par la cryptographie, et actuellement par les zero-knowledge proofs en particulier, j'ai envie de comprendre comment fonctionne des protocoles comme zerocoin, où l'on peut prouver qu'on possède un jeton sans dévoiler lequel.

[Cet article](https://eprint.iacr.org/2014/764) propose un "zerocoin scheme", c'est à dire un protocole de ring-signature, où chaque possesseur d'un jeton ne peux voter qu'une fois. Pour ce faire, on demande au signataire de dévoiler une valeur $serial$ en même temps que sa signature. Chaque serial **bound** son utilisateur à un jeton de signature sans dévoiler lequel.

J'ai donc fait [un brouillon d'implémentation possible](/belenios-ooom.pdf) dans Belenios (en m'inspirant beaucoup des documents existants).

L'implémentation naive que je propose est couteuse, chaque signature a une complexité linéaire en fonction du nombre de jetons possibles. L'article propose une solution en complexité logarithmique qui me dépasse encore. J'ai aussi trouvé [une implémentation](https://github.com/cloudflare/zkp-ecdsa/blob/main/src/proofGK/gk.ts) par cloudflare, avec l'optimisation.
