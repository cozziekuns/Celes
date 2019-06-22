#### Fight or Flight in ORAS

Consider the following ORAS situation on Tenhou:

*South 4  — East: 35000 (+6000), South: 29000 (You), West: 22000 (-7000), North: 15000 (-14000)*

North has declared riichi on the 9th turn, with the clear intent of aiming for 3rd place. It is now the 12th turn, and you have a currently yakuless tenpai with two dora. Fortunately, the tile that you need to cut to take tenpai has also become a safe tile. You can see clear signs that both East and West have broken up their hands and folded; they have no intention of fighting 4th place's riichi. Our hand has an ankou of the East, and we see one East on the board. If we choose to fold, there is basically no chance that we can deal in here.

If you riichi and score your guaranteed 5200 point hand, thanks to North's riichi stick donation, you'll be able to overtake East and secure 1st place. However, if you deal into North and they have a mangan-sized hand, you'll end the game in 4th place.

Now for the classic question: should we call riichi?

#### It's all about Risk/Reward

What's important to realise is that the rewards distribution of the ruleset changes the decision that we should make here. It seems obvious, but if our rewards distribution heavily incentivies 1st place, has only a small reward for 2nd place, and a moderate penalty for 4th place (most notably, the M-League ruleset), then we should be calling riichi here in an attempt to chase down East. 

However, if our rewards distribution is skewed such that there is little difference in reward between 1st and 2nd place, but a huge potential for loss given 4th place, then we should fold.

Usually though, the action we should take given the rewards distribution is not so clear cut. Consider the WRC rewards distribution for example. Going from 2nd to 1st will give us an uma bump of 10000 points, not to mention the 6200 points (or more!) we will gain via our win. However, going from 2nd to 4th will strip us of 20000 points, with another 8000 points (or more…) But really, just how likely is it that we deal into 4th place here?

The question then becomes: is there a way we can systematically determine which action to take given our rewards distribution?

#### The Fundamental Theorem of Mahjong

The key thing to understand is that Mahjong is ultimately a game of events and their probabilites. Events occur any time a round comes to a conclusion. For example, mangan tsumo is an event. A 1000 point ron is an event. Nagashi mangan is an event. Attached to each event is its unique probability of occuring at a given point in time. 

As mahjong players, our job is to increase the probability that good events happen, while decreasing the probability that bad events happen. We do this by performing actions (discarding tiles, calling tiles, calling riichi, etc). These actions influence the game state and alter the probabilities that certain events occur. Discarding tiles according to tile efficiency theory and decreasing our shanten increases the probability that our hand converts into a win (a positive event). Similarly, holding safe tiles and properly folding, while decreasing the probability our hand will convert into a win, also decreases the probability we deal into our opponents (a negative event).

This relationship of actions and events can be modeled as an equation that I've taken the liberty of naming "The Fundamental Theorem of Mahjong."
$$
EV(action) = P(Event_a|action)(EV_a) + P(Event_b|action)(EV_b) + \ldots
$$
The fundamental theorem of mahjong states that the expected value of a given action is defined as the linear combination of the product of all events that can occur given the action and their probabilities given the action. It is a tool that we can use to select the action that will benefit us the most in a given situation.

For example, you're given a hand that starts with 9 terminals and honors. The reward from the potential yakuman is huge, but the probability that it'll happen is so small… on the other hand, since the chance we win the hand is small, the chance that our opponents will win the hand is bigger than it would usually be; the probability of a bad event occuring is larger than it normally is. This generally makes the action of calling 9s9h superior to the action of playing the round and aiming for kokushi.

#### Tenhou's Reward System

Tenhou's ruleset creates an extremely unique variant of mahjong. For one, it has an infamously punishing penalty for 4th place; the higher dan ranking you have on Tenhou, the more punishing 4th place becomes.

But perhaps more bizzare is that its rewards system completely ignores the player's base scores. The payouts players are rewarded at the end of the game are solely tied towards placement. A game where a player ends in 1st with 80000 points is no different from a game where a player ends in 1st with 30000 points. If both players are playing in the Houou table, they will both reap the same reward of +90pt for their hard work.

Fortunately for us, this makes the expected value of certain plays in Tenhou much easier to calculate. As an example, a player rated 7-dan has the following rewards distribution: 

*1st: +90pt, 2nd: +45pt, 3rd: 0pt, 4th: -135pt*

I could talk about the intricacies of this rewards system all day, but the gist of it is that 1st > 2nd > 3rd >>> 4th. There is a 45pt swing between 1st and 2nd, and another 45pt swing between 2nd and 3rd, but a huge 135pt swing between 3rd and 4th. So dodging 4th should be our top priority.

#### Finally, some Analysis

Let's analyze the above situation using this 7-dan rewards distribution. We essentially have two actions that we can plug into the fundamental theorem: Riichi and Fold. Technically, we also have the action of not calling riichi and staying Damaten, but I will ignore this for simplicity's sake.

##### Fold EV

The first thing that I recommend any player do is calcluate their potential rewards if they fold, and use it as their baseline for deciding whether or not they want to take another action. This is because folding is the route with the least variance; if you know enough about defense theory, you can avoid playing into the players that you're folding against 99% of the time. It's also generally brainless if you have enough safe tiles stocked up. The easier something is to do, the less likely we will make a mistake, and the less mistakes, the more we win.

If we choose Fold as our action, then it seems like we only have the following two events: Either the North tsumos, or it goes to ryuukyoku. In reality, there are actually three realistic events that could occur: North tsumos a mangan or less, North tsumos a haneman or more, or it goes to ryuuykou. 

If North tsumos a haneman or more (not impossible given uradora), then we dip into 3rd place. Every other possible outcome secures us 2nd place. Remember that the rewards for 2nd and 3rd place in Tenhou are different; one is +45pt, and the other is +-0pt. 

But for the sake of example, let's assume that a little birdie told us that North's riichi is capped at a mangan tsumo maximum (e.g. their hand is riichi tsumo akadora, and their pair is the south). Actually, with this assumption, we don't even need to use the fundamental theorem: there are only two events, so the probabilty that one of the two events occurs is 1. Each event has a value of +45pt, so the Fold EV in this case is 1 * 45 = +45pt.

By basically doing nothing, we have an expected gain of +45pt. This is why folding is so strong.

*Note: In reality, the chance that a haneman tsumo happens is possible, but decently unlikely, like 8% chance, so our Fold EV is more like +42pt.*

##### Riichi EV

Let me start by saying that calculating the riichi EV is really, really hard. It requires us knowing exactly how many of our waits are live in the wall, how many of our opponent's waits are live in the wall, what our ura flip chances look like, etc, etc. So, I'm going to be make some huge simplifications, but even with the heuristics employed the actual EV shouldn't be too far off.

- Both the player and the riichi opponent have 2 waits in the wall.
- The player and the riichi opponent have different waits.
- The riichi opponent has a mangan on both tsumo and ron (4/40).

*I'll consider explaining why assume that each player has 2 waits in the wall isn't a bad heuristic in a later article, but for now, take my word for it.*

Then, we have a total of five possible events. First and foremost, the round could go to ryuukyoku. Given that it's the 12th turn, even though there are two players in riichi, this is a decently likely event.

If the game doesn't go to ryuukyoku, then things become a whole lot more interesting. Because both the player and the opponent have the same number of waits in the wall, the chance that either wins the round is essentially a 50/50. Moreover, there are actually four outcomes that can occur that are (almost) equally likely.

1. North tsumo's their mangan. You end the game in 2nd place (the gap between you and North is more than the difference that would be covered by your riichi stick + the mangan tsumo), for a reward of +45pt.
2. North ron's you for a mangan. You end the game in 4th place for a reward of -135pt.
3. You ron North. You end the game in 1st place for a reward of +90pt.
4. You tsumo. You end the game in 1st place for a reward of +90pt.

Now that we know the rewards of each event, we need to find the probabilty that each event occurs. I'll explain where I got these numbers from in another article, but my big brain tells me that there is roughly a 16% chance that, at turn 12 with two players in riichi and the two other players folding that the game will go to ryuukyoku. That means that there's an 84% chance that one of the four other events will occur. We'll assume that the four events are equally likely (take a while to convince yourself that this is more or less true). Now let's plug all these variables into the fundamental theorem.
$$
\begin{align*}
EV(riichi) &= 0.16(45) + 0.21(90) + 0.21(90) + 0.21(45) + 0.21(-135) \\
&= 0.16(45) + 0.21(90 + 90 + 45 - 135) \\
&= 26.1
\end{align*}
$$
The expected value of our riichi is +26.1pt, which is less than the +45pt we would expect from folding. In reality, the chance that our opponent tsumos a haneman will reduce our riichi EV even more (since there is a chance we could get 3rd place), to something like +25pt. In any case, since our riichi EV is a decent chunk lower than our fold EV, we should consider folding our hand.

#### Conclusion

Note that this contrived example, which has a bunch of simplifications, was already a huge pain to calculate. As you can imagine, doing these sorts of calculations in real life is simply impractical. And if you're familiar with Tenhou's rulesets, you probably already worked out that the correct answer was to fold in this case. 

But, this doesn't mean that the fundamental theorem is useless. For one, the answer to a lot of situations can be calculated ahead of time. For example, now you'll know that on Tenhou, as 2nd place, it's generally better to avoid fighting 4th place in ORAS if there's a possibility you'll drop into 4th place.

But more than that, what the fundamental theorem teaches us is that Mahjong is simply a game of actions, events and probabilities. Your goal as a mahjong player is to have the ability to work out which actions will shift these probabilities in your favour. The more accurate your understanding of these probabilities and how they shift according to your actions, the more likely you will perform the correct actions. The more likely you will win.