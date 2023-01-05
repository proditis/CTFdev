---
description: There is always status 503
---

# There will be some failures

Things can and will go wrong from time to time, how you deal with it can make a difference. Don't assume that the network is always there, that the database will never go down, that Memcached will always have keys etc etc :smile:

As developer you may think that you don't care about these things but you'll be wrong.&#x20;

Plan for a failure from day one and you wont have a failure ever again :wink:

Your users will ignore your failures if you do them gracefully. This could be as simple as having a custom error 500 page that shows the site is experiencing a temporary failure instead of the default white page with black letter that most web servers return.

Expect there will be failures and be honest with your users if they report problems. If they found a bug, let them know and give them credit for it. It may seem pointless to you, but for the player is a big deal. Everyone wants to brag about bugs they found, even if they are not security related.
