---
author: Mordecai
title: "Fundamental Surprise"
layout: post
---

Something I've seen crop up again and again, so now I'm writing about it:
"Fundamental Surprise" is what happens when you have to adjust your model of the
world to accommodate what you just learned. Another word for this is
'astonishment'.

Regular surprise is one of rarity distribution: You might be surprised to learn
that your friends' new partner is 220cm (7'2") tall, but you would be
fundamentally surprised, or astonished, to learn that they are a land-walking,
talking porpoise named Howard.

This is, approximately, everywhere. One specific example: Names. There's a
[classic blogpost by Patrick McKenzie][patio11-names] about this. A more
specific examples is a friend with a last name of two letters regularly posting
screenshots of websites insisting that last names be at least three letters.

The fundamental surprise here is on the side of the author of the website when
learning that people with two-letter surnames very much do exist, and would like
to use that website. The author's model has to change to accomodate this, and
only then can they fix their bug.

Closely related to this is the "Fundamental Surprise Error". It's what happens
when you learn of something that would require you to adjust your model, but
instead you explain it away as consequences of known behaviour.

For example, you host a small website. You get an alert that the website isn't
available, and see that your server is absolutely overwhelmed with load. You
figure, "Ah, someone must have posted one of my articles to the orange website".
Then you add another machine to the load balancer to help with the traffic, and
go on your merry way.

However, the problem is that your server was wide open, and so someone installed
a bitcoin miner on your machine. Adding more capacity is not going to fix that,
but it might fix the symptom by providing an uninfested machine. You will have
to change your model to actually fix the problem.

The other extreme of embracing every model change is just as bad. Model changes
are expensive, and _usually_ wrong (but crucially, not always), chasing every
potential fundamental surprise error will lead to a sustained belief in UFOs and
dismissing every rational explanation as others suffering from Fundamental
Surprise Error. The balance is delicate.

So, how do you guard against fundamental surprise, and fundamental surprise
error? Well, the pithy answer is "know more stuff". It is, however, also not
wrong. For the name example in specific, working with people from cultures with
those last names would have prevented this from happening. So would seeking
information and finding the Patrick McKenzie article about it.

Generally speaking, working, learning from, and checking with people from a wide
variety of backgrounds is a good way to prevent falling afoul of cultural
differences.

But particularly when working on systems that only exist once and that you are
currently working on, you are the first one to learn about the new and fancy
ways it can explode. The most helpful line of defence against fundamental
surprise is not to try and prevent it from happening, but to lower the costs of
adjusting your model, to make your system easier to change.

I have a hypothesis that Fundamental Surprise Error really stems from systems
being expensive to change, and so people really want to have believable reasons
to not need to change the system. They've got deadlines to meet, and other
concerns brewing. They don't have the time to change how they see the world, and
then change the system to accommodate that. But hey, here's an explanation that
requires none of that and is credible, let's go with that.

And so the symptom might be treated, but certainly not the cause. Things grow

more brittle, and the actual reason was not removed. In short, you need to be
wary, but not too wary. But investigating things that seem odd and being aware
of the fundamental surprise error helps.

[patio11-names]: https://www.kalzumeus.com/2010/06/17/falsehoods-programmers-believe-about-names/
