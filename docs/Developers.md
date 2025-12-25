# Developers

So you decided to bite the bullet and implement your awesome ideas. That is great, the more the merrier I say :smile:

I know this is not what most of you might be looking for, but before you start take a look at what is available to you, you may be able to find something to use as a base or hopefully contribute on an existing project...

In any case, I hope a fancy new interface is not all that you've come up with... right?

Well luckily, the following sections include some of the things that you have to keep in mind while developing your idea and save you from some time.

## It is NOT just the UI

The most common mistake that i've seen new and old developers do is that they focus only on the web interface. They spend the entire development effort into making awesome (and some times bizarre) web interfaces, assuming that this is all that matters.

The web interface is important but its not everything. You have to keep in mind that the only people who are constantly using the web interface are those who dont actually play!!!

People will visit your interface to find a challenge to work on and to claim their flags when done while checking the leaderboard every so often to check their standings.

Don't ignore your backend, most of the CTF developers discover this the hard way. Your backend involves everything that is used to run any type of service that the platform you're developing needs:

* databases, key-value stores
* storage allocations
* running challenges
* servers and services

## Forget the BETA notion

Every... Single... Developer (including this author) that i've seen assume that beta versions tend to have better "treatment" or that players will treat them differently... Nothing could be further from the truth... The moment the first player joins your platform, your project becomes production, the *BETA* notion is now only in your head.

People will expect everything they see to be fully functional, nobody cares that *you're testing.* Be ready to receive reports about anything and everything. There is no more temporary fixes or immunity from security incidents...

## Security is PARAMOUNT

Developing a CTF platform is not like any other application, mostly for one core reason: On a normal application you can assume that "some" (relatively small percentage) of your users might try a hack or two... On a CTF platform EVERY user is a hacker, its not "if they try" something, its almost guaranteed.

Don't leave this for later, the bigger the project gets, the harder it will be to secure it. Even if you leave things for later, make sure you document them carefully so that you dont forget them.

Although nobody will expect your platform to be flawless, there will be some types of bugs that will most definitely cause you troubles (and sometimes haunt you).

How you deal with these bugs and the way these bugs are introduced is important.

## There will be some failures

Things can and will go wrong from time to time, how you deal with it can make a difference. Don't assume that the network is always there, that the database will never go down, that Memcached will always have keys etc etc :smile:

As developer you may think that you don't care about these things but you'll be wrong.

Plan for a failure from day one and you wont have a failure ever again :wink:

Your users will ignore your failures if you do them gracefully. This could be as simple as having a custom error 500 page that shows the site is experiencing a temporary failure instead of the default white page with black letter that most web servers return.

Expect there will be failures and be honest with your users if they report problems. If they found a bug, let them know and give them credit for it. It may seem pointless to you, but for the player is a big deal. Everyone wants to brag about bugs they found, even if they are not security related.

## Use your imagination

Don't be afraigt to explore your ideas even if they are far outside the usual. Just because other platforms or projects did it one way, doesn't make it the only way or the right way.

There are a million ctfd replicas already, another replica with a new interface is not attractive to anyone.

## Documentation equals Contributions

If you don't provide documentation, there will be no contributions and some times even then there will be no contributions.

In any circumstance having documentation about your project will help a lot down the road as it will save you from saying the same things over and over with every user that wants to try your project :smile:
