---
description: So you want to create your neat challenges and machines?
---

# Content Creators

This document outlines the creative process and thinking that goes behind the scenes in the development of unique and interesting scenarios.

One of the questions that people ask, is how do we find such unique ideas for the targets we create and if we know of any guides or tutorials to point them to that help them in learning how to make targets and challenges.

The uninitiated will think `How hard can it be? i mean it took me 10 minutes to solve this challenge... Surely i can make one better`...

Well i don't want to be the bearer of bad news, but get ready to be tortured. Failed builds, bugs in logic and a lot more awaits you.

But I am not here to scare you, I am here to help you get over some of the difficulties or at least be better prepared for them. This is based on some of the things i've learned in developing and delivering CTFs and cybersecurity exercises for the past 10 years.

## Making Challenges and Machines

## Why do it❓

Why learn how to do something like this though? I can tell some of the reasons why I personally love developing challenges and targets for our platform.

As a developer of targets and challenges I get to:

* keep up2date with latest security developments. I love setting up servers, learning about cybersecurity developments helps me setup my systems better and apply some critical thinking when I follow official documentation and guides.
* keep up with new technologies and applications as well as new features that can be (ab)used.
* learn new techniques. No matter how good you are and how much you know there is always going be something new you've never thought about. Creating challenges and targets, exposes you to all the crazy paths the players will take to solve them. You get to see new and exciting methods and ways you can bypass security restrictions and improve your own processes in securing your assets.
* It does make you better pen-tester/bbhunter. As part of developing and setting up your challenges you come across details that you can take advantage later on. I have learned a large number of attack vectors for nginx by setting it up myself.
* It makes you a niche monster: Learning niche techniques and details about applications can make the difference between a payout and a duplicate 🤣 Again using the previous nginx example, i've learned that specific versions of nginx allow for duplicate host headers to be present. This will give me an advantage when i am faced with a similar system versus a hunter that does not have this information.

## ⛏️Picking a challenge/target subject

Picking a subject may vary from person to person, however, picking a challenge or target subject for me usually involves one or more of the following:

1. Inspirational: Sudden inspirations of obscure and crazy scenarios that not always make sense or are able to be implemented. Such as, you read something and it triggers an idea for something else...
2. Wise-ass/What if/Don't do: This is a particular category that i think not a lot of creators pay attention to. This has to do with testing assumptions and warnings to identify the extend of a security incident.
3. Research: I am interested in researching an area or technology out of personal interest, developing a target based on what i learned along my research is a good way to make sure i don't forget what i learn (not always successfully, but you get the idea)
4. Vulnerability/CVE: There is a major vulnerability being reported that for some crazy reason i feel that it needs to be on our platform, thus a new target is born.

### Inspirational

### Wise-ass

There are certain types of challenges that I like to call wise-ass. These are based on **`what ifs`** and **`dont's`**.

We all know that having a database accessible to the internet is bad, but what if it was accessible? These types of challenges try to address what happens then.

* What are some of the damages that could be sustained?
* What are their security implications on the system?
* Under which circumstances does this become an actual attack vector?

These types of challenges help in educating the users and the creators in cyber security policies with a better understanding for the consequences.

### Research

### Vulnerabilities/CVEs

You dont always have to all out of your way to create elaborate and *smart* scenarios for your challenges. Most of the times the vulnerabilities and CVEs that are reported online provide enough material to help you create a challenge in matter of seconds.

## 🤬Keep calm

There are a few things that you have to be prepared for as a challenge creator that nobody prepares you for.

As a challenge creator get'll get

1. People are going to steal your shit with 0 fucks given and some times almost verbatim
2. People are going to accuse you of stealing their challenge, (eg a challenge you made got copied by a big CTF so the majority of people saw it there first...)
3. People are going to give credit to the person who copied it from you...
4. People thinking that you suck 🐒⚽⚽ because they solved your challenge (yes there are those)
5. People who are going to make you feel like they are asking you back their time **`spend`** playing your challenge

### Not so obvious

So why keep calm if all those 💩 goes around? The answer is simple, you don't do it for the shitheads, you're doing it for the rest of the players who did enjoy and appreciate your job 😂

No matter how bad the criticism, the majority of players will always enjoy and appreciate your efforts and this will be visible at the end of your CTF. Take bad criticism as an opportunity to improve your challenges in the future.

I much rather spend my time to make my challenges shithead-proof than hacking-proof...

## 👍 Rules of Thumb

### Documentation rules them all

I will not sugar coat this, this is the hardest part of every challenge for me. There are never enough details that you can put into the document. Your players will always ask something that you haven't predicted and you'll have to go to the source code of the challenge.

What I do to keep those to a minimum are as follows:

* All challenges are on a single repository
* Each challenge has its own `README.md`  general purpose documentation that outlines some basic concepts of the challenge / machine explaining
  * the premise of the scenario
  * solution steps (eg `1. user does that...`)
  * references to sources and material used during build
  * exploitation, detailed exploitation steps with copy/paste-able material
* Challenges that run complicated applications also have an `ADMINISTRATOR.md` with administrative details and commands used to manage them
* `WRITEUP.md`: A complete solution, preferably written by someone else who will also provide feedback

### The documentation is not just for you

Depending on the team that provides support to the players some of these documents will be eventually shared with them. This is why you have to create the separate documents. You can give access to the README and ADMINISTRATOR documentations but not the WRITEUP. Its not about "trust" its about keeping it fair for everyone.

### Keep local copies

In this day and age its hard to believe that anyone would want to keep a "backup" of a publicly accessible github repo but you'll be surprised at what can happen between the time you conceive your idea, develop and finally run it.

Repositories get moved around without notice, others truncate their history, others close all together, others will remove their vulnerable release version, other projects change names repos and history altogether. These and many more similar cases await you.

Create a folder, say `./assets/`, and use it to store there releases and the specific packages that your challenge or machine depends on.

You will thank me later for that...

### Its not you vs players

Content creators often fall into the trap of feeling like its them against the player, when in reality it is not.

People try to harden their boxes, patch this and that to force the players on a very specific exploitation that they had in mind. **STOP** DONT DO THAT. Why do you expect that everyone should be thinking the same way you do?

One of the best things about creating content for CTF's is that you get to see all those crazy minds at work. See and learn from the ideas that all those participants will come up with in trying to solve your challenge.

My belief is that a smarter and more talented player should always be able to outsmart me. And that is a good thing :smile:

### The difficulty rating

The difficulty rating is one of the hardest things to do "accurately" and the truth is you will never get it just right, because its impossible to do.

Every player that approaches your challenge/machine has different background, experience and inspiration at that given time.

You will always get mixed results even if you are perfect at rating them:

* you will get experienced players that find hard challenges easy and easy challenges hard
* you will get noob players that will find easy challenges hard and hard challenges easy

The difficulty rating when it comes to a CTF has to take into consideration a lot of factors.

#### Is it online or onsite CTF

In online CTF's players work from the comfort of their systems which makes it a lot easier to research a certain subject.

Onsite events tend to put the players under more "stress" and thus a challenge that would normally take 40 minutes might take 1 or 2 hours.

#### The duration of the even

What is the total duration of the event? Is it going to be 3-4 hour event or entire day?

I try to make sure that for every individual participant there are enough challenges to go around. I try to make each of my challenges/machines in such a way that among all of them it will take, on average, 45 minutes to be solved by a normal player.

So depending on the duration of the even the i have as many targets and challenges as it will take to go just a tini bit above my mark. So for an 8 hour event, 460 minutes event / 45 minutes per machine ≃ 10 machines. Just to be safe i always prepare a few extra challenges usually a bit more hard than the rest, so as to keep any outliers occupied and serve as a buffer until the CTF concludes.

#### The estimated duration of the challenge



#### Team or individual participation

#### The difficulty changes over time

Even if you take everything into account and you manage to somehow nail the difficulty rating when the challenge/target was published, be ready for a disappointment. It is generally observed that difficulty of most challenges go up or down as time passes by.

But how could this be possible you may ask? Here are a couple of examples:

* The challenge you developed require a specific version of a tool that is no longer easy to find making it harder to solve (eg older versions of chrome are harder to find)
* The challenge/machine depends on technologies or architectures that are not generally available (ie SGI IRIX Unix was relatively easy to come by both systems and exploits back when the machines were still in circulation, nowadays not so much)
* The challenge/machine is on subjects that are generally more well known (eg such as sql injections, started as something rare, now everyone seems to know how to do at least the basics)

### The unsolvable challenge/machine

I've seen countless challenge creators brag about their unsolvable challenges and how crazy their scenario was that nobody thought about it...

Let me tell you a little secret, if a challenge stays unsolved because it was so hard that nobody could have solved it, then you failed as a challenge creator!

There is only **ONE** reason you make a challenge and that is to be **SOLVED** (eventually).

Keep in mind that this does not include challenges that players were unable to complete due to time running out. We're talking about challenges that under no normal circumstances someone could have solved them in the given time of the entire CTF.

### docker containers

#### **volumes**

Make sure your container images have no volumes. Volumes solve a very specific problem with containers and that is _persistent storage_. Volumes allow containers to store data to be used and shared among them, even across restarts.

Volumes can be defined using the `VOLUME` statement inside your `Dockerfile` or by using an image that already has one, such as mysql. The first case is easy to spot, check your `Dockerfile` for `VOLUME` statements, in the later case though it gets a bit trickier.

The only 100% way to avoid having volumes inherited by your containers, is to write the entire `Dockerfile` yourself. The usual `docker inspect`, `docker image inspect` commands will come in handy, as well as `docker volume ls`.

As a last resort you can always run the image and see what volumes got created 😂

#### **readonly**

#### **healthchecks**
