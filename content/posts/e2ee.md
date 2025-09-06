---
title: "End-to-end encryption"
date: 2025-08-01T00:00:00+02:00
---

<!-- introduction -->

Most humans spend more than 40% of their waking life on the internet, using it
for all kinds of tasks—even private ones, like talking to our friends. How can
I make sure to keep my conversations private ? A good answer is **end-to-end
encryption**. Let's dive into the topic, and why we need such a thing.

## The early internet (web 1.0)

Let's first have a quick look at internet history. At first, the internet was a
friendly place and most communications happened in the clear.

![web1a](/web1a.svg)

But then hackers came, they were able to listen to our communication or even do
powerful tricks such as [man-in-the-middle
attacks](https://en.wikipedia.org/wiki/Man-in-the-middle_attack), allowing them
to intercept, block and inject messages, impersonating Alice or Bob. The
internet was no longer a safe place.

![web1b](/web1b.svg)

But the internet is full of wizards! They soon had developed cryptographic
protocols such as [SSH](https://en.wikipedia.org/wiki/Secure_Shell),
[SSL/TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security) and
[PGP](https://en.wikipedia.org/wiki/Pretty_Good_Privacy), allowing them to be
much safer against such attackers. Everything was fine again.

![web1c](/web1c.svg)

## The age of platforms (web 2.0)

But then, Muggles (people who did not know how the internet worked) came.
Because they were not wizards, they were not able to host their own website
(even more so email servers). Yet they needed to communicate. They had to use
_platforms_. This is what we call the web 2.0.

![web2](/web2.svg)

Shortly after the rise of the web 2.0, most of our private communications
happen on platforms like Gmail or Whatsapp, most of our thoughts are shared on
Twitter or Reddit, and most of our value is exchanged on platforms such as
Amazon or Uber.

Platforms are wonderful, they help people connect and let the economy grow.
They even protect our communication. We hear Google's ["Don't be
evil"](https://en.wikipedia.org/wiki/Don%27t_be_evil) and there is some
"privacy laws" such as the
[GDPR](https://en.wikipedia.org/wiki/General_Data_Protection_Regulation). But
we also entered the world of [Surveillance
capitalism](https://en.wikipedia.org/wiki/Surveillance_capitalism) and [data
brokers](https://en.wikipedia.org/wiki/Data_broker) are selling our data.

## End-to-end encryption

Alice wants to talk to Bob using a platform. Instead of encrypting her message
to the platform, she can encrypt her message to Bob. This is called
**end-to-end encryption**, and it's the way to hide your messages in the age of
the platforms. The idea is simple: you encrypt your messages on _your device_
and the messages are decrypted on your correspondent's device. This way, the
platform only sees the encrypted message, revealing no information about the
cleartext.

![e2ee](/e2ee.svg)

If you want to use **end-to-end encryption**, [Signal](https://signal.org/) is
a good start.
