---
description: How hard can it be?
---

# Making Challenges and Machines

## ❓Why do it?

Why learn how to do something like this though? I can tell some of the reasons why love developing challenges and targets for our platform.

As a developer of targets and challenges I get to:

* keep up2date with latest security developments. I love setting up servers, learning about cybersecurity developments helps me setup my systems better and apply some critical thinking when I follow official documentation and guides.
* keep up with new technologies and applications as well as new features that can be (ab)used.
* learn new techniques. No matter how good you are and how much you know there is always going be something new you've never thought about. Creating challenges and targets, exposes you to all the crazy paths the players will take to solve them. You get to see new and exciting methods and ways you can bypass security restrictions and improve your own processes in securing your assets.
* It does make you better pen-tester/bbhunter. As part of developing and setting up your challenges you come across details that you can take advantage later on. I have learned a large number of attack vectors for nginx by setting it up myself.
* It makes you a niche monster: Learning niche techniques and details about applications can make the difference between a payout and a duplicate 🤣 Again using the previous nginx example, i've learned that specific versions of nginx allow for duplicate host headers to be present. This will give me an advantage when i am faced with a similar system versus a hunter that does not have this information.

## ⛏️Picking a challenge/target subject

Picking a subject may vary from person to person, however, picking a challenge or target subject for me usually revolves around one of the following three:

1. Inspirational: Sudden inspirations of obscure and crazy scenarios that not always make sense or are able to be implemented. Eg you read something and it triggers an idea for something else...
2. Research: I am interested in researching an area or technology out of personal interest, developing a target based on what i learned along my research is a good way to make sure i dont forget what i learn (not always successfully, but you get the idea)
3. Vulnerability/CVE: There is a major vulnerability being reported that for some crazy reason i feel that it needs to be on our platform, thus a new target is born.

### Inspirational

### Wise-ass

There are certain types of challenges that I like to call wise-ass. These are based on **`what ifs`** and **`dont's`**. Lets explain these with an example

* For anything related to memcache you'll read that its dangerous for `memcached` to be accessible on the internet. But what happens on the lan? _What If_ someone got access to your memcache then what? Thats a `what if` type of challenge
* You read a manual for a programming language when all of a sudden you see a warning saying "Don't use this with untrusted data..." or something to that effect. So you say don't i say do. That is a `dont's` type of challenge

These types of challenges help in educating the users in cyber security policies with a better understanding of the consequences.

### Research

### Vulnerabilities/CVEs

You dont always have to all out of your way to create elaborate and _smart_ scenarios for your challenges. Most of the times the vulnerabilities and CVEs that are reported online provide enough material to help you create a challenge in matter of seconds.

## 🤬Keep calm

There are a few things that you have to be prepared for as a challenge creator that nobody prepares you for.

As a challenge creator get'll get

1. People are going to steal your shit with 0 fucks given and some times almost verbatim
2. People are going to accuse you of stealing their challenge, (eg a challenge you made got copied by a big CTF so the majority of people saw it there first...)
3. People are going to give credit to the person who copied it from you...
4. People thinking that you suck 🐒⚽⚽ because they solved your challenge (yes there are those)
5. People who are going to make you feel like they are asking you back their time **`spend`** playing your challenge

## Not so obvious

So why keep calm if all those 💩 goes around? The answer is simple, you don't do it for the shitheads, you're doing it for the rest of the players who did enjoy and appreciate your job 😂

No matter how bad the criticism, the majority of players will always enjoy and appreciate your efforts and this will be visible at the end of your CTF. Take bad criticism as an opportunity to improve your challenges in the future.

I much rather spend my time to make my challenges shithead-proof than hacking-proof...
