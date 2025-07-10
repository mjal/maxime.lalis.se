+++
itle = 'Signal is no silver bullet'
date = 2025-06-19T00:00:00+02:00
+++

# Signal is no silver bullet

## On privacy online

<!-- introduction -->

Most humans spend more than 40% of their waking life on the internet, using it
for many things, including private matters.

<!-- problématique -->

But wait, how good is privacy online ?

<!-- history -->

Let's first have a quick look of internet history. At first, the internet was a
friendly place, not so many people used it, so most things were open, and most
communications happen in clear. Then, more people started using, including
hackers. So we started to close access, and encrypt sensible communications.
The internet was full of wizards and everything was fine. This is the web 1.0.

![web1](/web1.jpg)

But then, Muggles (people that did not knew how the internet worked) cames.
Because they were not wizard, they were not able to host their own website
(even more so email servers). Yet they needed to communicate. They had to uses
_platforms_. This is the web 2.0.

![web2](/web2.jpg)

Shortly after the rise of the web 2.0, most of our private communications
happens on platforms like Gmail or Whatsapp, most of our though are shared on
platforms like Twitter or Reddit, most of our collaborative work happens on
platforms such as Google doc, and most of our value is exchanged on platforms
such as Amazon or Uber. This is also the age of the platforms.

![age-of-platforms](/age-of-platforms.jpg)

And all of this is fine for a while. Platforms are wonderful, they help people
connect and let the economy grow. They even protect our communication. We hear
Google's ["Don't be evil"](https://en.wikipedia.org/wiki/Don%27t_be_evil) and
there is some "privacy lays" such as the
[GDPR](https://en.wikipedia.org/wiki/General_Data_Protection_Regulation). But
we also entered the world of [Surveillance
capitalism](https://en.wikipedia.org/wiki/Surveillance_capitalism) and [Data
brokers](https://en.wikipedia.org/wiki/Data_broker) are everywhere.

## End-to-end encryption

E2E-E

Platforms like Signal

Let's imagine Alice wants to talk to Bob through platform Polo.

## Original version

<!-- encryption -->

Privacy matters. To have privacy on the internet, we usually rely on
encryption. Signal is one of the best tools out there for end-to-end encrypted
communication. Yet encryption is not always enough. We also need to take good
care of metadata.

What is **metadata**? Metadata is the context of your message. From whom to
whom, when, with what device, which app, etc.

Metadata is very important. Some even said that "if you have enough metadata
you don’t really need content". Indeed, knowing who knows who is already
valuable information, and can be enough to infer a lot of information,
including political views or other sensitive information.

Someone sitting in the same coffeeshop, sharing the same wifi hotspot and
looking at network traffic (he is a tech enthusiast) wouldn't be able to know
more than "This person is using Signal (actively or not)". Which you can argue
is already sensitive information, it already tells something about Alice. For
that, you can use a VPN (but they're not silver bullets either).

<!-- Schema SVG de alice, mallory (with a deamon smiley, the wifi hotspot
(internet smileys). You see Signal messages (the arrows become blue with a
signal logo) going through the wifi hotspot, and we can see Mallory seeing them
(also lighting up ?) -->

If you're communicating with someone also sharing the same wifi hotspot, he
would also be able to know "This person is probably communicating with that
person".

<!-- Same schema. But Bob also use Signal, and receive Alice messages (through
the wifi hotspot and back). Mallory can see both, and can infer that Alice is
probably talking to Bob. -->

<!-- weak attacker knowledge

He wouldn't be able to know more than "This person is using Signal actively or
non-actively" (which is already a sensitive information). If you're
communicating with someone also sharing the same wifi hotspot, he would also be
able to know "This person is probably communicating with that person".

This is already a lot. In fact, how often you use Signal says a lot about you,
because it tells a lot about your friends. But for that, we want even more
adoption, so it becomes the norm.

-->

<!-- strong attacker -->

But we also need to consider stronger attackers, including Signal themselve,
the people hosting them (which would be Amazon in the case of Signal), people
owning part of the internet infrastructure, or a even a collusion of such
actors. We consider such powerful attacker in [provable
security](https://en.wikipedia.org/wiki/Provable_security) 

In the case of Signal, Message content's privacy is proven in such strong
model, but for metadata, we don't really know.

Such strong attacker can gain even more information either be passive
observation (I see that when Alice is sending a message, Bob is receiving one).
They can also actively interact to gain some information (If I block Bob, Alice
is not receiving a read receipt).

<!-- Schema with DY attacker -->

Yet, Signal is still an essential tool that we should use as much as possible,
but please remember that it's not a silver bullet. Such metadata gathering
could even transform Signal in the very mass surveillance machinery it tries to
circumvent (the same argument can (loosely) be made for other encrypted
messaging apps like Matrix or (even more strongly) for Telegram, Whatsapp...).

What we really need is [metadata-free
communications](/posts/metadata-free-communications).
