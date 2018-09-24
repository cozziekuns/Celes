---
layout: post
author: cozziekuns
excerpt_separator: <!--more-->
---

Instead of giving a detailed explanation and a bunch of definitions about what
Lean is, I figure the best way to explain what I hope to accomplish is with a 
simple example. Lean is not a quick hack to increase your win-rate, nor is it 
a reminder that you need to work on your game to see results. In the words of 
Bobby Scar, who applied a 
[similar-but-different Lean framework](https://leanmelee.wordpress.com/) (that 
inspired this one) to the game Super Smash Brothers Melee:

_First, Lean is not a way to start winning a few more games quickly. It’s also not 
merely a reminder that we should continue to learn and improve. The desire to improve 
is a requirement. A commitment to the philosophy of continuously achieving validated 
learning is the foundation._

Lean Mahjong is a framework that is all about identifying and removing 
waste in our process. To do this requires a strong understanding of mahjong 
fundamentals and mechanisms that I plan to delve into in the upcoming posts. For 
now, here's a little taste of what I have planned.

### A Problem

![2-1](/assets/img/2-1.png)

What is the best tile to cut here? The xia screams saftey; after all, toimen
has already cut a xia, meaning that anyone waiting on that tile would have to
have committed themselves to a tanki xia wait. Plus, if the xia does pass as 
expected, and one of the two players in riichi is unlucky enough to draw a haku, 
this gives us an instant ryanmen tenpai for a dealer mangan, which would essentially
be a win condition given how far behind kamicha is. With all that said, surely xia 
is the best tile to cut here?

That's exactly the trap that I fell in admist the chaos of this hanchan. As a result, 
I ended up playing into a baiman from kamicha (riichi ippatsu chiitoitsu dora dora ura 
ura), and ended the hanchan in 4th, losing precious Tenhou dan pts. Was this really my 
fault, or did I just get screwed over by the gods of mahjong yet again?

### Assessment

Was cutting xia such a grave sin? While there are many good reasons that you should 
cut xia here, that doesn't necessarily mean that it is the best tile to cut here. 
Even if it is the most EV positive tile to cut here, it's also what I consider a 
"lazy" cut.

There are a few key points here. The first is the fact that kamicha is below 3900
points. If they play into anything bigger than a 3 han 30 fu hand, they will bust.
Assuming that kamicha and simocha are waiting on a similar number of tiles, and 
that both me and toimen are folding, there is a 50% chance that either player 
tsumos, 25% chance that kamicha plays into simocha, and a 25% chance that simocha 
plays into kamicha (assuming one of the ronpai is drawn by either combatant).

This means that by doing absolutely nothing, my chance of flat out winning the 
hanchan is already around a solid 25%; extremely good considering that I am playing 
betaori. Usually when you decide to play betaori, you are essentially conceding a 
bite-sized chunk of points (tenpai payments or tsumo, plus the points you may have 
earned had you pushed) to dodge a large hit. In thise case, you might not even have 
to take a small hit; kamicha busting would be to your absolute advantage!

Similary, in the event that kamicha hits simocha, kamicha and simocha would now both 
outside of striking range of first. Essentially, they would be scrapping between 
themselves for 3rd, and the battle for first would be narrowed down to a battle 
between me and toimen. This is especially good in Houou, because even placing 2nd nets 
a fairly decent reward of +45pt.

The second key point is that the dora is the haku. Since I'm already holding two of
them, if any of the two combatants is using the dora, it must either be a dora tanki
or dora toitsu. Discounting dora tanki (since there's no way I'm playing the dora), 
let's suppose that someone is holding the dora toitsu. Naturally, a menzen hand holding 
a toitsu of yakuhai tiles lends itself to a specific hand: chiitoi. If we consider the 
possibility of chiitoi, xia immediately becomes much more dangerous. Not only is it 
commonly considered a good chiitoi wait, if we do play in with the xia, it is 
extremely likely that we will be paying into a haneman. Even that alone is enough to 
offset the relative safety that the xia brings in terms of deal-in percentage. Chancing 
it risks too much for next to zero value.

### Alternative

So, what should we discard instead? Is there a better tile to cut? In this case, even
taking the xia into consideration, there is an alternative tile to cut. 

#### 8s is the safest cut in this instance.

Kamicha has cut 8s and the tile that they declared riichi on was the 5s. This means 
that if simocha is waiting on the 8s, it would have to be kanchan, shanpon, or tanki.

We see two 8s tiles in the discard pile and we have one 8s in our hand, so a shanpon wait 
is physically impossible. Simocha discarded 6s two turns before the riichi, which means 
that they would've had to have purposely given up a 58s ryanmen for an 8s kanchan. 
Last but not least, if simocha is waiting on a 8s tanki, that means that they
purposely commited to a jigoku tanki on the 8s, knowing fully well that kamicha is 
likely to chase given their desperate situation. From a macro-game perspective, this
train of thought makes next to no sense.

### Diagnosis

Understanding that we made a mistake is important. But even more important is 
uncovering the root cause; that is, why did we make this mistake in the first place? 
To diagnose this, we have to be honest with ourselves and determine, from deep within 
our mental stack, what exactly led to us making this mistake. In our reflection, we 
need to scan for root causes, which are usually quite hard to surface. In my 
experience, working your way back through your thought process is generally the best 
way to filter for these root causes. For reference, my own inner dialgoue went a 
little like this:

* I cut the xia and dealt into a baiman hand.
    * Why did I cut the xia?
* I felt like xia was safe to push, and I wasn't aware of any alternatives.
    * Why did I feel like xia was safe? Why wasn't I aware of 8s?
* I made a lazy play and didn't bother considering 8s, because xia is usually safe. I 
also failed to consider that, if xia is the ronpai, it is very likely that I play into
a haneman.

In this case, the root cause of the problem was hidden in the third layer of my thought
process. I was lazy; even though xia isn't genbutsu, I naturally assumed it was the 
safest tile, given that the rest of my hand is filled with all number tiles and the 
dora. It felt even safer because I had a toitsu in my hand, and toimen had discarded 
one early, leaving tanki as the only option. Had I stopped to think about how dangerous 
(value wise) xia is from the context of this board, or noticed that 8s was basically a
100% safe tile, I would have never played it.

(As an aside, I personally believe that the "EV-positive" play is almost always also
the lazy one. Lazy doesn't mean that the play is necessarily bad; it just means that, 
for a given board state, there may be a better cut lingering in the shadows that 
we miss if we tunnel in on the EV-positive play. I often wonder if people that play 
different imperfect information games, like poker, carry similar thoughts to the ones 
I do regarding this matter...)

### Treatment

Now that we have identified a root cause for the waste, we need to determine some 
sort of practical treatment to ensure that we never make the same mistake again. In 
this case, the root cause of my misplay was due to my laziness; I tunnel visionned
on a tile that is usually safe, and discounted any information that might have 
suggested a better cut.

In the past, I've tried increasing my in-game focus level with varying results. It's 
simply unrealistic to believe that your mind will always be in the zone, especially 
when playing in a relatively low pressure environment like Tenhou. With that in mind, 
my proposed treatment is a quick and fast rule that I can apply and eventually make 
a habit of. The goal is to make it so that, when faced with a certain situation, my 
mind will naturally follows this process. My proposed treatment is as follows: 

*Whenever riichi is called, immediately look for at least two tiles that are safe. 
Then, if folding, compare those options and cut the one you have concluded is safest.*

While I haven't tested this approach yet (to be honest, I just came up with it today),
it seems a lot more promising than the usual approach of going down the tier list in
terms of tile saftey. With this, I am essentially playing a mind trick on myself that
forces me to validate the actual safety level of a certain tile in lieu of other 
potential safe tiles. 

Obviously, this approach can backfire; the last thing you want to do is waste time 
stuck in analysis paralysis while the Tenhou clock keeps ticking down. It also uses 
a lot more mental energy than "throw the safest tile". But as this approach becomes 
more habitual, I am hoping that the benefits will provide more than enough compensation 
for its downsides.

### Conclusion

I hope this gives you a deeper insight on what the goal of this project is. Remember, 
a huge part of eliminating waste comes from treating lazy habits like this one. 
During the course of this voyage, I aim to reason about and eliminate as much waste 
from my mahjong process as I can, keeping it as lean as possible. Hopefully you have 
been inspired to do the same.

#### See you on Tenhou.