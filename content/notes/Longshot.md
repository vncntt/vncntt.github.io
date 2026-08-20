+++
date = '2026-08-19T00:00:00-08:00'
draft = false
title = 'Long Shot: The Dice Game'
+++

{{< figure src="/longshot_components.jpg" width="50%" alt="Long Shot: The Dice Game components" caption="I made an online version of the game [here](https://longshot-eval.vercel.app/)." >}}

## Intro

Over the weekend, I really enjoyed a board game my high school friends and I played: [Long Shot](https://boardgamegeek.com/boardgame/295374/long-shot-the-dice-game)[: The Dice Game](https://www.perplext.com/long-shot-the-dice-game). 
A normal round is meant to be 30 min but ours' ended up being 3 hours because we were tanking to think through various strategies! 

To celebrate, I made an online version of the game [here](https://longshot-eval.vercel.app/) and tested how good various models are at this.

## Basic Game Rules

The game is played by 2-8 players, and the goal is to maximize your money. Some ways to earn money including owning a horse that finishes on the podium (\$35 for 1st, \$25 for 2nd, \$15 for 3rd), placing bets on winning horses, and completing certain side tasks. 

{{< figure src="/gameboard.png" width="70%" alt="Game viewer" caption="Scoring card" >}}

At the start of each round, the roll of the dice determines which horses moves by how much and the options available each turn. Once a horse runs 16 moves, it passes the finish line. When the first three horses cross the finish line, each player's earnings are totaled, and the richest is the winner. 
{{< figure src="/track.png" width="70%" alt="horse track" caption="Horse Track" >}}

Players spend each round taking a single action which could be buying horses, placing bets on horses, filling out concessions on the bingo board to get special abilities, using the abilities of horses, jerseying horses (jerseying Horse 1 on Horse 2 means whenever horse 2 is rolled, horse 1 moves forward one unit as well), or colluding with other players to beef up specific horses. 

{{< figure src="/horses.png" width="70%" alt="horse track" caption="Horses have different abilities and costs." >}}

## Observations about the Game

- Early in the game, there's lots of uncertainty about which horses are going to perform well. A strategy is to bet hard on, commiting, a single horse. Another is to hedge your bets, letting others expend their resources and trying to scoop the winnings at the end.  
- When playing with more than two people, small alliances naturally form and ending up on the wrong side can lock you out of the game. Player A may own a horse while Player B has heavily invested in it, meaning there's a shared interest to pump the horse up, leaving Player C in a 1v2 situation. 
- The game can flip very quickly when some players invest heavily early and hit late-game scaling. When a horse is fully jersey-ed (it moves a unit forward no matter what horse is rolled), it will almost always reach the podium. 
- Even with near-perfect play, I think you can still lose if the dice rolls are unfavorable. The game is often about maximizing your chances of winning even in low-likelihood scenarios. 

This game is a nice testbed for models since:
- The game can be fully represented in text. 
- It's not very popular (#368 on BoardGameGeek) meaning it's not in training data much, and there isn't much strategy discussion online. 
- Initial game strategy (betting all on a horse or hedging) under lots of uncertainty is important and can decide the rest of the game. Mistakes early on can be detrimental. 
- Singular bad decisions can cost you multiple turns or lock you out of the game completely. Are models careful or sloppy?
- Humans get better at the game with more play. Can models play multiple games, take notes of their learnings/strategy, and improve? 
- In 3 or more player games, do models collude, form alliances, or lie? This happened in many of my human games. 

The main limitation is that the skill ceiling is not very high for a singular expansion (the same deck of eight horse abilities). I think it gets saturated after ~20 hours of human play though not confident (I've only played for ~5 hours).

## Model Results

I beat the best at this game pretty consistently and {X} model is the best out of the others. 

Model performance results:
MISSING RESULTS HERE
- GPT vs Fable vs Gemini vs Grok vs Muse Spark
- Opus 5 / Fable 5 reasoning effort comparisons
- graph of model performance as it plays consecutive games. 

## Conclusion

Consider buying the physical game [here](https://www.perplext.com/long-shot-the-dice-game) to play with your friends in-person!

{{< figure src="/viewer.png" width="100%" alt="Game viewer" caption="Fable did a pretty good job with the viewer." >}}
