---
layout: post
author: cozziekuns
title: Zen Mahjong (Part I - Perfect)
excerpt_separator: <!--more-->
---

Zen Mahjong is a thought experiment that arose from a simple question: "Is a perfect game of 
Tenhou possible?" As it turns out, that question has a very simple null hypothesis answer. 
Since Tenhou uses a mahjong ruleset a ruleset where busting (having negative points) ends the game, 
and results in Tenhou are based solely on placement, there is a nice and easy solve for this 
problem. A Tenhou + 1 Double Yakuman tsumo on the first turn would simultaneously bust the other 
players, ending the game while also giving us the best possible outcome (first place).

With that out of the way, we can begin asking ourselves the real tough questions. "When does a 
perfect game cease to be perfect?" and "What constitutes a perfect play?" To answer these 
questions, we need to dive into and explore exactly what we mean when we say "perfect" when talking 
about games. To do that, we need to define what perfect is; this will prove to be the pillar and 
foundation for Zen Mahjong.

### Solved Game

When I was a young lad, I was fascinated to death with a mini-game NPC that exists in the video 
game Tales of Phantasia. If my memory serves me correctly, this certain NPC appears in the past 
city of Alvanista, and challenges you to a game he calls "Ishi-Tori". The premise of the game is 
simple; starting with a randomised number of counters, take turns removing either one, two, or 
three counters from the community pot. The person who removes the last counter is the loser.

Beating the so called "Ishi-Tori" master was quite challenging for my younger self. The NPC seemed 
to play flawlessly every time, and I somehow found myself always ending up as the one to take the 
last counter. Frustrated, I swallowed my pride and went online to find a perfect strategy to defeat 
the NPC. As it turns out, the strategy is roughly as follows:

"The number of counters at the beginning of the game will always be of the form (X * 4) + 1. When 
challenging the Ishi-Tori master, always elect to go second. When the Ishi-Tori master takes his 
turn, note how many counters Y he takes. Then, simply take (4 - Y) counters from the community 
pot. The Ishi-Tori master will be forced into taking the last counter every time."

This was a mind blowing revelation to my infant mind. If you played the game of Ishi-Tori perfectly, 
there was a surefire way of winning everytime. In technical terms, Ishi-Tori is a "solved game." So 
long as the starting number of counters is of the form (X * 4) + 1, the player who goes second can 
always force a win.

But there is something that I didn't bother to think about as a kid; is there a "perfect" strategy 
for the player going first? No matter what the first player does, the second player can always 
force a win. I believe in chess, they refer to the first player's situation as a "zugzwang." 
Assuming that the second player knows the winning strategy, whatever move the first player makes 
will be a losing move. The EV of each move that the first player makes is strictly the same: 0. 
Does this mean that any play that the first player follows can be considered a "perfect" play?

(Interestingly, there is a winning strategy for the player who goes first if the starting number of 
counters is any number that does not produce a remainder of one. For example, if the starting 
number of counters is 10, the player that goes first can choose to take a single counter. This 
creates a game state where the "first" player is now second to act, and the "second" player is now 
in zugzwang.)

### "The game of Chess" and "That game of Chess"

There's a video out there that shows Magnus Carlsen, the current chess champion at the time of this 
post, checkmating multi-billionaire Bill Gates in only 9 moves. Perhaps most impressively is that 
Carlsen accomplished this feat with a meager time budget of 30 seconds, against Gates's 2 minutes.

Needless to say, when Magnus Carlsen checkmated Bill Gates in 9 moves, he didn't play a perfect 
game of chess. There are numerous videos on the internet that explain how, if Gates had made a few 
different moves, he would have easily attained the upper hand against Carlsen. Carlsen himself 
admitted that he essentially relied on a "trick"; he presented Bill Gates with a problem that he 
didn't believe Gates would be able to solve.

Let's twist the question a little bit. Clearly, Carlsen didn't play "the game of chess" perfectly. 
But did Carlsen play "that game of chess" perfectly? I think that it's arguable that he did. Given 
his knowns, Carlsen had ample reason to believe that Gates would undoubtedly fall for his trick. 
Gates, while an obviously intelligent individual, is relatively unfamiliar with the game of chess. 
He knows the rules of course, but not much else about the game. Since Carlsen only has 30 seconds 
on his clock, he needs to find a checkmate sequence fast. As Gates is unfamiliar with the game, and 
has himself only 2 minutes on the clock, Carlsen made a pretty safe bet that the sequence of moves 
he made would result in his victory. Gates fell for the trick, Carlsen converted that mistake into 
an advantage, and the rest is history.

This might seem like a stretch, but chess players play like this all the time. A lot of chess 
basically lends itself to putting the opponent in the most uncomfortable position possible. When 
playing against weaker players, stronger players put themselves in "theoretically" weaker positions 
simply to take the weaker player out of their comfort zone. If the strong human player was playing 
against a supercomputer that could read the entire game tree, from the current board state all the 
way to a forced checkmate sequence, then the human player would obviously lose. But, because the 
weaker player doesn't know how to play that board state, the stronger player is advantaged even if 
they are in a theoretically disadvantaged state. 

Of course, this can't work all the time. The reason it doesn't work is because it's impossible to 
accurately predict someone's thoughts. Imagine a scenario where you're playing Rock-Paper-Scissors 
with a child who stubbornly refuses to throw anything but Rock. You've played 100 games with them, 
and they've thrown rock everytime. If we assume that child will throw Rock for their next move, 
there is a "perfect play" to win the next round: throw Paper! All too predictably, the child has a 
sudden change of heart and throw Scissors.

The reason that your "perfect play" was not perfect, is because what you initially considered was 
a "known" (your opponent's action/response), was actually an unknown. This happens all the time. In 
chess, the weaker player might just end up randomly finding the correct way to deal with your 
trick. In mahjong, a player is in guarenteed 1st place, unless they play into your mangan hand. 
It is in their best interest to fold, but they brazenly push multiple dangerous tiles. They end up 
hitting you with their mangan hand, dropping you into 4th place.

### "The Axiom of Perfection"

This is the train of thought that led me to the first axiom of Zen Mahjong -- the Axiom of 
Perfection.

"A perfect play is the play with the highest scoring Expected Value given all known relevant 
variables."

Observe:

In the example where we are playing Ishi-Tori, given that both players know the optimal strategy, 
there is really only one relevant variable.

EV of Ishi-Tori = -1 * P(Go First) + 1 * P(Go Second)

In the example when we were playing Rock-Paper-Scissors with the child, there are three relevant 
variables, and we can model the game as follows:

EV of Throwing Paper = -1 * P(Child(Scissors)) + 0 * P(Child(Paper)) + 1 * P(Child(Rock))

If we are given that the child will always throw Rock, then our model becomes:

EV of Throwing Paper = -1 * 0 + 0 * 0 + 1 * 1 = 1

Thus, if we are given that the child will always throw Rock, the perfect play is to throw Paper.

### TLDR

The question, then, is to identify what the relevant variables are in the game of Mahjong, and how 
to most accurately estimate them. This will be the essential project of Zen Mahjong.