+++
title = 'Unlinkable ring signatures for Belenios'
date = 2024-10-21T21:02:47+02:00
+++

[Voici un brouillon de spécification d'unlikable ring signatures pour
Belenios](/belenios-zerocoin/belenios-zerocoin.pdf).

L'objectif est de garder secrète la participation ou non à une élection, via un
protocole de ring-signature où il faut dévoiler une valeur *témoin* en plus de
la signature, afin d'éviter le re-vote. [Cet
article](https://eprint.iacr.org/2014/764), [implémenté par
cloudflare](https://github.com/cloudflare/zkp-ecdsa/blob/main/src/proofGK/gk.ts)
est une source d'inspiration.
