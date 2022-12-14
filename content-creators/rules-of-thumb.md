# 👍 Rules of Thumb

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

Content creators often fall into the trap of feeling like its them against the player, when in reality it is not. &#x20;

People try to harden their boxes, patch this and that to force the players on a very specific exploitation that they had in mind. **STOP** DONT DO THAT. Why do you expect that everyone should be thinking the same way you do?

One of the best things about creating content for CTF's is that you get to see all those crazy minds at work. See and learn from the ideas that all those participants will come up with in trying to solve your challenge.

My belief is that a smarter and more talented player should always be able to outsmart me. And that is a good thing :smile:

### The difficulty rating

The difficulty rating is one of the hardest things to do "accurately" and the truth is you will never get it just right, because its impossible to do.

Every player that approaches your challenge/machine has different background, experience and inspiration at that given time.&#x20;

You will always get mixed results even if you are perfect at rating them:

* you will get experienced players that find hard challenges easy and easy challenges hard
* you will get noob players that will find easy challenges hard and hard challenges easy

The difficulty rating when it comes to a CTF has to take into consideration a lot of factors.

#### Is it online or onsite CTF

In online CTF's players work from the comfort of their systems which makes it a lot easier to research a certain subject.&#x20;

Onsite events tend to put the players under more "stress" and thus a challenge that would normally take 40 minutes might take 1 or 2 hours.

#### The duration of the even

What is the total duration of the event? Is it going to be 3-4 hour event or entire day?&#x20;

I try to make sure that for every individual participant there are enough challenges to go around. I try to make each of my challenges/machines in such a way that among all of them it will take, on average, 45 minutes to be solved by a normal player.&#x20;

So depending on the duration of the even the i have as many targets and challenges as it will take to go just a tini bit above my mark. So for an 8 hour event, 460 minutes event / 45 minutes per machine ≃ 10 machines. Just to be safe i always prepare a few extra challenges usually a bit more hard than the rest, so as to keep any outliers occupied and serve as a buffer until the CTF concludes.

#### The estimated duration of the challenge



#### Team or individual participation

#### The difficulty changes over time

Even if you take everything into account and you manage to somehow nail the difficulty rating when the challenge/target was published, be ready for a disappointment. It is generally observed that difficulty of most challenges go up or down as time passes by.&#x20;

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
