+++
date = '2026-08-19T00:00:00-08:00'
draft = false
title = 'Long Shot: The Dice Game'
+++

{{< figure src="/longshot_components.jpg" width="50%" alt="Long Shot: The Dice Game components" caption="I made an online version of the game [here](https://longshot-eval.vercel.app/)." >}}

## Intro

Over the weekend, I really enjoyed a board game my high school friends and I played: [Long Shot](https://boardgamegeek.com/boardgame/295374/long-shot-the-dice-game)[: The Dice Game](https://www.perplext.com/long-shot-the-dice-game). 
A normal round is meant to be 30 min but ours ended up being 3 hours because we were tanking to think through various strategies! 

For fun, I vibe-coded an online version of the game [here](https://longshot-eval.vercel.app/) and tested how good various models are at this.

## Basic Game Rules

The game is played by 2-8 players, and the goal is to maximize your money. Some ways to earn money include owning a horse that finishes on the podium (\$35 for 1st, \$25 for 2nd, \$15 for 3rd), placing bets on winning horses (which have different multipliers based on the final placement), and completing certain side tasks. 

{{< figure src="/gameboard.png" width="70%" alt="Game viewer" caption="Scoring card" >}}

At the start of each round, the roll of the dice determines which horses move by how much and the options available each turn. Once a horse runs 16 moves, it passes the finish line. When the first three horses cross the finish line, each player's earnings are totaled, and the richest is the winner. 
{{< figure src="/track.png" width="70%" alt="horse track" caption="Horse Track" >}}

Players spend each round taking a single action which could be buying horses, placing bets on horses, filling out concessions on the bingo board to get special abilities, using the abilities of horses, jerseying horses (jerseying Horse 1 on Horse 2 means whenever horse 2 is rolled, horse 1 moves forward one unit as well), or colluding with other players to beef up specific horses. 

{{< figure src="/horses.png" width="70%" alt="horse track" caption="Horses have different abilities and costs." >}}

## Observations about the Game

- Early in the game, there's lots of uncertainty about which horses are going to perform well. A strategy is to bet hard on, committing, a single horse. Another is to hedge your bets, letting others expend their resources and trying to scoop the winnings at the end.  
- When playing with more than two people, small alliances naturally form and ending up on the wrong side can lock you out of the game. Player A may own a horse while Player B has heavily invested in it, meaning there's a shared interest to pump the horse up, leaving Player C in a 1v2 situation. 
- The game can flip very quickly when some players invest heavily early and hit late-game scaling. When a horse is fully jersey-ed (it moves a unit forward no matter what horse is rolled), it will almost always reach the podium. 
- Even with near-perfect play, I think you can still lose if the dice rolls are unfavorable. The game is often about maximizing your chances of winning even in low-likelihood scenarios. 

This game is also a nice testbed/eval for models since:
- The game can be fully represented in text. 
- It's not very popular (#368 on BoardGameGeek) meaning it's not in training data much, and there isn't much strategy discussion online. 
- Initial game strategy (betting all on a horse or hedging) under lots of uncertainty is important and can decide the rest of the game. Mistakes early on can be detrimental. 
- Singular bad decisions can cost you multiple turns or lock you out of the game completely. Are models careful or sloppy?
- Humans get better at the game with more play. Can models play multiple games, take notes of their learnings/strategy, and improve? 
- In 3 or more player games, do models collude, form alliances, or lie? This happened in many of my human games. 

The main limitation is that the skill ceiling is not very high for a singular expansion (the same deck of eight horse abilities). I think it gets saturated after ~20 hours of human play though not confident (I've only played for ~5 hours).

## Model Results

I ran 20 games total: 10 games with five players each (Muse Spark 1.2, Opus 5, Fable 5, GPT-5.6 Sol, Gemini 3.1 Pro) on two versions (no-chat: models simply took actions during each turn, chat: models can talk privately with each other). 

<div style="display: flex; flex-wrap: wrap; gap: 2em; justify-content: center;">
<div>

|    Model   | wins | avg score |
|------------|------|-----------|
| Opus 5     | **5** | 91.5 |
| GPT-5.6    | 3    | 68.5 |
| Gemini 3.1 | 1    | 72.4 |
| Muse       | 1    | 74.5 |
| Fable 5    | 0    | 87.1 |

<p style="text-align: center; font-size: 0.9em; opacity: 0.8;">No-chat version</p>
</div>
<div>

|    Model   | wins | avg score |
|------------|------|-----------|
| GPT-5.6    | **5** | 80.0 |
| Fable 5    | 3    | 81.0 |
| Opus 5     | 0    | 78.8 |
| Gemini 3.1 | 1    | 60.4 |
| Muse       | 1    | 64.4 |

<p style="text-align: center; font-size: 0.9em; opacity: 0.8;">Chat version</p>
</div>
</div>

The results are in line with what I expected other than Fable doing so poorly on the no-chat version. A quick Claude analysis says that Fable tries to get the maximum possible score rather than trying to go for first place (which it is explicitly instructed to do) which often includes spending many moves sabotaging other players.

Opus 5 is the most talkative model and gives away its strategy in the chat-version of the game. It generally uses good strategy which is why it wins so frequently in no-chat, but this information asymmetry is lost when it starts babbling about what its long-term plans are every turn. I think there's a lot more model behavior you could study in these game interactions tweaking various parameters!

I also have a working version of "the model plays the game, writes a notes.md of its learnings, and plays the game again with these new notes," but didn't get many runs on this to study whether models can get better at this game with many playthroughs. 

-----
Consider buying the physical game [here](https://www.perplext.com/long-shot-the-dice-game) to play with your friends in-person!

{{< figure src="/viewer.png" width="100%" alt="Game viewer" caption="Fable did a pretty good job with the viewer." >}}
