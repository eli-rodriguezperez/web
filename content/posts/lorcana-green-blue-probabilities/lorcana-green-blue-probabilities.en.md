---
title: "Data and conclusions on Green Blue decision making"
date: 2025-10-06T12:25:13.108Z
draft: false
language: en
images:
tags:
  - lorcana
  - Green Blue
  - GB
---

## Introduction

Hello GB friends, I'm Seven. I wanted to write an article on probabilities for certain decisions that are common in Green Blue. I've been playing ramp decks (mainly DKP RB), a couple of sets, and with these kind of decks relying so much on chance to draw ramp and some key cards, I believe that is key to delegate certain decisions to probability.

I like to think about a card game as you would for a chess game for the most part. There is an opening phase, in which you have to already have the lines memorized, because if you start improvising and your oponent knows the correct line you're probably already lost, or at least on a big disadvantage; A midgame, in which you try to develop your game plan; and a late game, in which a single decision is game deciding. In card games you don't always have the same pieces in hand, nor does your oponent, so a chess opening would more correctly relate to a matchup opening. This is really important as we want to consistently have the correct pieces for the right matchups. What I want to say with this is the less decisions you have to make before entering midgame, the most consistent you can make your gameplan. This is why the correct Altering decisions can make us have better hands and convert more games into victories.

For the most part I just want to present the data and then my conclusions as to why I decide to Alter a certain way based on the data in the end. This way you can see my interpretation of the data, which can obviously be wrong, and I invite anybody that can refute it with data to do so. I tried to double check everything that I am writing here.

## Concept glosary

During this article I will use a shorthand for certain concepts that encompass groups of cards, I want to use this section to explain what those mean.

- _Ramp_: _Ramp_ would include tipo and sail. We would have 8 targets for a ramp card.
- _DyB_: _Develop your Brain_.
- _Clara7_: Just big Clarabelle.
- _Clara3_: 3 cost Clarabelle. 4 targets.
- _Clara1_: 1 cost Clarabelle. 4 targets.
- _SmolClara_: The combination of both _Clara3_ and _Clara1_, for which we would have 8 targets.
- _ClaraEnablers_: This would include both clarabelle shift targets and donald5. As this cards enable lines where you can cheat _Clara7_. We have 12 targets for this group. This group will serve as a baseline to calculate the probability of at least being able to cheat out clarabelle earlier than you would normally. Which IMO is the baseline to have a decent game. Not being able to do this normally means youre at a disadvantage, so we want to at least hit one of these.
- _3UtS_: When I refer to running 3 targets for Under the Sea.
- _4UtS_: When I refer to running 4 targets for Under the Sea.

## Altering for ramp

This has long been a discussion in the community, also for other ramp dependant decks. You normally throw everything away to have the best chance to draw back ramp after 7 new cards. The two cards that generated discussion as to why to Alter a different way were _Pawpsicle_ and _Develop your Brain_. Which change the math around being able to draw the ramp we need after the Alter phase. Taking pawp out of the ecuation, there is another card that people run sometimes in GB, which is _Bobby_. _Bobby_ doesn't exactly draw you a card, but it lets you dig one card deeper. Develop allows us to dig two cards deeper.

Keeping _DyB_ with no ramp has been the main question for x8 ramp blue decks for a while, and I was on the boat for throwing it because I thought the variance of not seeing that last extra card didn't compensate for the two extra cards you're seeing later, but I did the math, and it turns out it does. It's kinda stupid to argue about this decision, as the difference is so minuscule that most of the time it won't matter. But nonetheless, knowing that seeing two cards after shuffling is better than the extra chance that seeing 14 cards deep before shuffling gives is something that applies to most decks and is information that I will use looking forward.

This data is taken from a script that a fellow GB player made for making simulations on the Alter phase and then two turns of play, to calculate the mean for how many times depending on the situation you're in you will draw ramp. I modified the script to run several simulations so that I could calculate Standard Deviation, to get a bit of context. The mean doesn't always tell the full story, but variance, in this case stdev gives us a look at the inconsistency over all those simulations.

This stats are the result of a simulation where 100.000 players "played" 500 games with a determined way of playing if not finding ramp in the first seven cards. This takes into account all the different nuances that can occur, like throwing 7 can sometimes result in having a _DyB_, or throwing 6 but drawing into another _DyB_. Even with all that the stats are clear. Even though that it's a stupidly small number, keeping _DyB_ is always the best, it even nets smaller variance. So in about 0.55 games every 500 OTP and 0.4 games OTD, you will not find ramp if you throw away your develop as opposed to keeping it, while also being a tiny bit less consistent. Without taking variance into consideration, which only improves the odds for keeping _DyB_.

(script will be provided but not present in this article)

| Situation    | Mean   | Standard Deviation |
|--------------|--------|--------------------|
| OTP Throw 7  | 92.46% | 1.187%             |
| OTP Keep DyB | 92.57% | 1.177%             |
| OTD Throw 7  | 93.73% | 1.084%             |
| OTD Keep DyB | 93.81% | 1.081%             |
_Statistics of the simulation in which we calculate how many times over the simulations we're getting ramp back with each strategy_

## Cow math

Having Clarabelle 7 on board, specially shifted on 5 ink is really important for GB, for this reason we do want to maximize the chances of enabling the shiftline, or at least, being able to play donald5 to be able to play Clara next and get value with maybe MKB or YW. This decision is critical, as we're going to see, taking an incorrect strategy in the Alter phase means you're not going to get _Clara7_ on board as much as you want to. For this section and onwards, I will use hypergeometry to analyze the decisions. So we're talking probability, not statistics.

### Pre alter situations

#### We do not have ramp in hand

We're going to start with a hand where we do not have ramp but we do see a _Clara7_. In this situation, we could think throwing 7 cards is the correct choice. Here we have to think if having _Clara7_ on board is critical to the game plan, which on most matchups is. So we have two options, we throw everything, and hope to find ramp and _Clara7_ back, or we keep the _Clara7_ and throw everything else. Let's see how the probability changes with this two scenarios in mind.


| Situation | Odds  |
|-----------|-------|
| Keep      | 70.6% |
| Throw     | 64.5% |
_Probability of drawing ramp if we keep Clara7_

Now, the probability of getting a _Clara7_ back in hand if we throw one away is 35.2%. So the question is, do we think that even if we find ramp by throwing 7, which will make a difference in 6.1% of games, will result in a game worth playing, or will it be a nongame anyway in which we ramp into nothing and lose anyway. For me right now, I think 64.5% is still decent odds that I prefer to Keep the _Clara7_ and make sure we have it. As we will see later, it's much easier to find a _ClaraEnabler_ and at 64.5%, we have decent odds to have a normal gameplan if the ramp comes back, as opposed to possibly never being able to find a _Clara7_ in time until it's too late after shuffling them back into the deck.

====

#### We do have ramp in hand

In this situation we already have the most important piece in hand, so let's see all the situations we can find ourselves in and see what probabilities we're playing with.

| Situation             | Odds  |
|-----------------------|-------|
| _Clara7_ alone          | 39.1% |
| _Clara7_ + _SmolClara_    | 23.2% |
| _Clara7_ + _ClaraEnabler_ | 29.6% |
_Probability of finding Clara7 in combination with other cards while keeping ramp and throwing everything else_

| Situation               | Odds  |
|-------------------------|-------|
| Keep ramp + 1 _SmolClara_ | 33.1% |
| Keep ramp + 2 _SmolClara_ | 27.6% |
_Probability of finding Clara7 while keeping ramp and some SmolClaras_

| Situation               | Odds  |
|-------------------------|-------|
| Any shift target        | 56.7% |
| A specific shift target | 33.6% |
| ClaraEnabler            | 73.1% |
_Probability of finding Clara7 enablers if we keep ramp and Clara7 in hand_

====

### Post alter situations

#### We have no Clara7 in hand

Here we're analyzing the probability of drawing into _Clara7_ before the shift turn with five inks. Having a minimum of three draws OTP and a maximum of 8 with a combination of being OTD while playing _Bobby_, _Sail_ and _DyB_.

| Number of draws | Odds  |
|-----------------|-------|
| 3               | 21.4% |
| 4               | 27.6% |
| 5               | 33.6% |
| 6               | 39.1% |
| 7               | 44.0% |
| 8               | 49.1% |
_Probability of drawing Clara7 with each consecutive draw_

#### We have Clara7 in hand

In this situation we're looking to, while having _Clara7_ in hand, being able to play her before turn 6.


| Number of draws | Odds  |
|-----------------|-------|
| 2               | 28.2% |
| 3               | 39.4% |
| 4               | 49.1% |
| 5               | 57.4% |
| 6               | 64.5% |
| 7               | 70.6% |
| 8               | 75.7% |
_Probability of drawing a SmolClara before being able to play her to be shifted with 5 ink_

| Number of draws | Odds  |
|-----------------|-------|
| 3               | 54.5% |
| 4               | 65.4% |
| 5               | 73.9% |
| 6               | 80.4% |
| 7               | 85.4% |
| 8               | 89.2% |
_Probability of drawing a ClaraEnabler to at least be able to play Clara7 earlier than usual_

#### Under the Sea after the alter phase

In this section I want to analyze some common lines in which we don't keep UtS against Dogs while still being able to sing it later. Ranging from some of the least common to a bit less optimal one. There are a million situations we could calculate here, but I decided on this 5 to have a general idea of the differences between _3UtS_ and _4UtS_, which I think are enough to make conclusions.

| Situation | _3UtS_/_4UtS_   |
|-----------|-------------|
| Line 1*   | 11.3%/14.7% |
| Line 2*   | 16.6%/21.4% |
| Line 3*   | 40.1%/49.1% |
| Line 4*   | 48.1%/57.9% |
| Line 5*   | 31.3%/39.1% |

_Line 1_: Clara>Tipo>Baymax 2 cards deep OTP

_Line 2_: Bobby>Tipo>Baymax 3 cards deep OTP with Bobby or OTD organically

_Line 3_: Clara>Tipo>Baymax>Visions 8 cards deep OTP

_Line 4_: Clara>Tipo>Baymax>Visions>DyB 10 cards deep OTP

_Line 5_: Tipo>Donald4>Donald5 6 cards deep OTP

### Conclusions

After presenting all this data, I want to elaborate on the decisions I am making based on it.

First of all, talking _Develop your Brain_, we know that looking at two cards after shuffling is better in terms of consistency and variance to seeing that 13th or 14th card. So what I conclude is that I am always going to keep a _DyB_ in hand, either without ramp, or in combination with ramp, to get closer to that _Clara7_. It also improves your chances of drawing into your next wanted card which could be _UtS_ or the _Basil7_, _Hades_ and the likes.

When looking into getting _Clara7_ and her enablers, I conclude that If I already have a _Clara7_ in hand, even with no ramp, I prefer to keep her over the possibility of never getting her back again. There are alternative lines where you can save a matchup with no _Clara7_ on board, but in general I want to avoid those at all costs as when you don't have the _Clara7_, the shiftlines can become completely useless, essentially having 12x _Tipo_ in your deck which you don't want to draw into but you're a lot more likely to do so.

Having no _Clara7_ in hand leaves me with no options but never keeping shiftlines in hand unless it's _Clara3_ OTP, which trades a bit of variance of having less chances to get _Clara7_, with the option of having the best shiftline and also drawing that extra card with her, and possibly getting that shift anyway. I would never do this if I'm OTD or in a matchup where I know _Clara3_ is not drawing a card. The chances of getting a _ClaraEnabler_ after shuffling them back in is still much much better than the chances of getting _Clara7_ in hand, so I think based on the data that it's always better to throw them away.

With _UtS_ numbers, in metas where singing it is a necessity to win a big amount of your expected matchups, having 4 copies in your deck is a must. Specially because having to ink one with _Tipo_ or losing it with an opposing _Ursula2_ can be game losing.

Also in general, being able to sneak in a couple of _DyB_ to fill the curve over the game makes your wanted draws much more likely and I will want to run 4 copies of them always, specially in decks with lower card quality and almost no cards that replace themselves, in this case GB.

And with this, this article comes to an end. After paying much more attention to probability and Alters, I've felt like I'm having much more consistent games. Now I'm not a person that likes to grind 500 games per set, but I've getting good records with my last 13 games being 11-2 in the site we must not name in the Bo3 ladder, with lost games being nongames with no ramp or having unlucky games against aggro decks. I've been able to climb up to 1480MMR pre Bologna which sadly I was not able to attend. I definitely feel like this is THE deck for me going forward. I have no doubt that it has a huge floor to pilot it correctly and a huge ceiling which we can try to maximize paying attention to probability and statistics, and it can only improve if we get better cards printed.

I hope you have enjoyed this read and have a great Lorcana Set Championship season,

Seven.
