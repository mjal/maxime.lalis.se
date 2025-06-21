+++
title = 'Metadata-free communications'
date = 2025-06-21T00:00:00+02:00
+++

Some of us can been profondly discriminated against due to their identity
(racial, gender, ...) or solely due to political views. This is especially
worrysome in the age of surveillance capitalism.

People shoud use it encryption, but [Signal is no silver
bullet](/signal-is-no-silver-bullet). We can do better with **metadata-free
communication tools**:

Such tools also mask who you're talking to, when, how often, ... or if you're
if you're actively communicating or not.

We'll separate such tools in two models:
- The cacophony model: Tools like [vuvuzela](https://vuvuzela.io/) that emits a
  lot of data, but data is indistingushable from random values.

  We can categorize them in 3 modes:
  + Periodic pulses. Emit noise periodicly, in a round-based setting (e.g. 1
    message every 10 minutes). This is how vuvuzela works.
  + Randomly timed pulses. Emit randomly emitted noise. This would allow more
    real-time usage while still being able to comply with differential privacy.
  + One shot: Emit/receive everything at one (e.g. one a day).

- The murmur model: Communications will look very similar to other kind of
  trafic (ex: browsing the web, watching videos) and/or hidden using
  steganography
