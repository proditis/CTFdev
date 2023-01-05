---
description: So you want to develop your own neat CTF platform?
---

# Developers

## It is NOT just the UI

The most common mistake that i've seen new and old developers do is that they focus only on the web interface. They spend the entire development effort into making awesome (and some times bizarre) web interfaces, assuming that this is all that matters.&#x20;

The web interface is important but its not everything. You have to keep in mind that the only people who are constantly using the web interface are those who dont actually play!!!

People will visit your interface to find a challenge to work on and to claim their flags when done while checking the leaderboard every so often to check their standings.&#x20;

## Forget the BETA notion

Every... Single... Developer (including this author) that i've seen assume that beta versions tend to have better "treatment" or that players will treat them differently... Nothing could be further from the truth... The moment the first player joins your project becomes production, the _BETA_ notion is now only in your head.

People will expect everything they see to be fully functional, nobody cares that _you're testing._ Be ready to receive reports about anything and everything. There is no more temporary fixes or immunity from security incidents...

## Security is PARAMOUNT

Developing a CTF platform is not like any other application, mostly for one core reason.

On a normal web application you assume that "some" of your users might try to hack you, on a CTF platform EVERY user is a hacker. Its not "if they try" something, its "when".&#x20;

## There are going to be security incidents

Its easy to get carried away during development and implement features in a way that is not optimal. Say you disabled CSRF token validation on a particular endpoint during development and you forgot to re-activate it.&#x20;

