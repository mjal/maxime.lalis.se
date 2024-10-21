+++
title = 'Trusted third party and lost credentials'
date = 2024-10-21T20:51:00+02:00
+++

This is an idea to handle lost credentials in a decentralized/trustless setting.

A trusted third-party in charge of elibility could be able te regenerate lost credentials with care. It would be tolerated in case it's RARE. And warnings should be issued.

```js
// before change
let credential = "8555a9..." // voter_pubkey (+ optional weight)
// after change
let credential = ["8555a9...", "5acec..."] // [voter_pubkey, trusted_third_party_pubkey] (+ optional weight)
```

It would allows
```
# Vote from voter:
Event(Vote): sign(ballot, "8555a9...")
# delegate from either user or trusted third party
Event(Delegate): sign(delegation, "5acec...")
# But would not allow the trusted third party to vote in behalf of user
Event(Vote): sign(ballot, "5acec...") # not possible
```

Note: In this case we could even rely on user-generated credentials.
Protocole:

```
Alice: sk
Alice  -> CA: pk = pk(sk) (* + prove identity by email and/or phone, ... *)
CA -> ElectionServer: sign(delegate(old\_pk, pk), ca\_pk)
A  -> ElectionServer: sign(vote, pk)
```

Note: This could also be a solution to the problem of the case where a user need to login through a different device/lose his device. Instead of restricting Charly to vote, we could have him verify his identity, let's say by both email and phone, and collaborate with the trusted third party to regenerate a new credential. Of course, this comes with a security risk, and a warning (ex: "the identity keys of Charly have changed") should be issued.

Note: This looks not very compatible with one-out-of-many signatures. It could be compatible however if one (either charly or a trusted third pary) has a (one-out-of-many) signed revocation certificate, since it would spend/burn the value serial.
