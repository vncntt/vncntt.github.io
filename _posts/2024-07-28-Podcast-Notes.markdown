---
layout: post
title:  "Podcast Notes"
date:   2024-07-28
---

# Karpathy on No Priors (9/6)

- waymo was basically a perfect drive 10 years ago (regulation, edge cases, ... took 10 years) 
- tesla is ahead of waymo 👀. tesla has a software problem and waymo has a hardware problem. tesla already has their hardware (cars) all around the world and waymo only has sf
- you have to build it up incrementally but endtoend is the way. video stream -> neural net -> steering commands
- everything from self-driving cars transfers to humanoid robots
- tesla isn't a car company. it's a robotics at scale company
- tesla has so much in-house expertise for hardware, scale, software, data
- the first humanoid robots won't be doing laundry. the first applications will be in-house doing your own stuff then b2b to other companies with large warehouses then b2c at the end
- he's crazy bullish on tesla
- humanoid is good bc data collection, world is built for humans, transfer learning between all tasks. very specific form factors are local minima
- a lot of the tools are already there. it's the grunt work, messy details that is still missing
- transformers are so goated. the first nn that scales for 7 ooms. it's software tissue that you can reconfigure for almost anything. it's better than the brain in a lot of ways (working memory). backpropogation might be better than the brain (crazy to think about)? 
- internet data isn't actually that good. it's just what was convenient, good enough, and took us surprisingly far. the internet is 99.9% random info and 0.1% actual good thinking? what you really want is the inner monologue in brains as they problem solve
- you have to make sure your synthetic data still has a lot of entropy and pertains diversity/richness or your model will silently collapse into a narrow npc distribution. bullish on synthetic data tho. it has to work
- augmentation with tech is already happening on an insane scale
- current models are wasting lots of space memorizing random stuff (sha hashes). distillation works. we'll have 1b models that work very welll
- "companies of llms": different llm swarms with specialties (code, writer, ...) that operate together
- how far could a person go with the perfect tutor?
- karpathy grew up in slovakia??
- in a post-agi society, education is mostly entertainment. 
- 200 years ago, all the ppl doing science were the nobility who didn't have to worry about life. 
- eureka labs hype

# Ricki on Complex Systems (8/23)

- teaching pays better than trading??
- crowdfunding (for regular people to pool together and fund companies instead of buying stocks after ipo) is adverse selection. good companies won't be passed on by vcs and angel investors
- reponse to "why do u ever trade if adverse selection" is you need a valid story for why someone else is taking your trade and why someone else hasnt offered the trade you are if it is profitable
- the real time order book is obtainable with all the prices and times listed but the names aren't available. why? because if you see trades from goldman sacks and the 9-5 wannabe hft, you will want to trade more with the 9-5 and goldman sacs doesn't want this
- arbitrage: trading two different products that are essentially the same product (price) in a way such that you are profiting risk-free
- example of information leakage when it doesn't seem like info is being leaked: private planes have to be logged and you can see where big ceos are flying based on their plane. if they are frequently flying to somewhere the usually don't, it might mean they are trying to acquire that new company and you can use that information to your benefit. this doesn't seem like info leakeage since all this info is open-source but bits are in face being given out.
- same thing for when and what a trader's book recommendation is or simply when a friend asks you about something and you seem to know a lot about it or how many people are at your desk (how many resources the firm dedicates to your work)...
- another example: who someone follows on twitter


# Patrick McKenzie Dwarkesh Episode (7/28)
VaccinateCA:
- centralize information about where to get vaccines
- started as a random hackathon project between friends at 10 pm
- became biggest site for this in US
- why wasn’t this done by the government?
    - no one called this specifically their responsibility
    - everybody only wanted to do some part, but not the whole thing so no one even started
- big tech companies didn’t do this because they didn’t want to appear more competent than the government then gov looks poorly on them + get bad business???
- copenhagen principle: the person doing anything gets responsibility for everything -> person doing anything gets more hate than person doing nothing. touching the problem immediately takes liability for all problems
- discord servers > government, health agencies, big tech lmao
- example of how EMH is usually wrong
- this is an example of real INSANE agency
- the US government has abdicated software as a core responsibility
- Tiering system for vaccines
    - Tier 1A (healthcare professionals, 75+, vets), 1B (school teachers (??), 1C (ppl who will probably die if the get COVID)
    - no one talks about how prioritization killed people. 
- how much did cultural factors (wokeness, BLM, …) play a factor?
- **california only successfully injected 25% of their vaccines**
- government could’ve given amazon the job of transporting viles in cool temp. they’re good at transporting things
- to protect the integrity of the tiering system, people threw out shots rather than giving it to someone not next in the queue
- people in tech need to get better at working with the government

What is crypto good for?
- the value hasn’t arrived yet. they’ve used hundreds of billions of dollars, but how much value have they actually produced? thinking about crypto in terms of resources consumed vs value produced. if it was another tech company, it would’ve failed already. ai….?
- what’s kyc, aml? know-your-customer. anti-money laundering
- all transaction errors have to be monitored. banks have intelligence-agency-sized groups of people writing memos no one is gonna read. what
- crypto uses privacy questionably

Government + big tech
- should the tech industry be part of the government?

what is this choosing to have nice things?

Financial plumbing:
- how hard is money laundering?
- the most sophisticated money launderer was sbf. he laundered tens of billions of dollars without being caught. he just ended up losing the money
- how to launder money? establish shell corp then buy real estate somewhere then rent houses to ppl then earn clean money. money put in is wired to a lawyer? confused

Maximizing value
- “most people don’t charge enough for their services”
- in some pro-capitalist cultures, there is less engrained skepticism about accumulating resources as a goal. not true for others. culture clashes cause weird stuff?
- salary negotiation. you have no less right to the marginal dollar compared to a company. agency thing?
- his article has literally earned ppl money totaling 8 figures every year

Young people
- there are less people in their 20s with prominent software businesses now compared to 10 years ago. is this true?
- holy shit patrick has played 4-6k hours of video games
- sammy mention
- a lot of factorio hype
- wtf. he had 68 direct reports in his WoW raid guilds. video games be wild

Thinking well
- good writing is good thinking.
- what did founders spend too much effort overoptimizing on? status

Blameless post-mortems


# Sholto Douglas and Trenton Bricken Dwarkesh episode (4/16)

- agents arent a thing yet not because of short-context windows but because current models arent reliable enough st you can chain long actions with success. an extra 9 or little bit of accuracy increase and boost the whole chain
- adaptive compute, decide how much compute you want to use for each task. using more forward passes
- ml companies are just greedily optimizing through the possible ai architectures like evolution
- models making better data
- gpt4 ~ 1 trillion parameters?? brain has approx 30-300 trillion synapses so we might still be below brain scale
- superposition implies that nowadays models are still extremely underparameterized. its trying to fit large dimensions in small ones. a bigger model just means cleaner representations
- toy models of superposition paper. compresssing very sparse features (things it needs to know) and compressing it down to more confusingly which is why its so hard to interpret
- superposition occurs when you have high-dimensional data that is sparse
- chain of thought is adaptive compute
- how much better would collaborating agentic models be if they could share residual streams instead of communicating through text
- dream of rl: provide this really sparse, end, reward signal and then the model learns the correct actions to take
- language is the modality evolution has come up with to learn about reasoning
- david bau's lab paper: if you fine tune on math problems, model gets better at entity recognition. related: training on code bases makes model better reasoning: being able to code just makes you able to think better
- just make shit happen no matter what. execute
- if you actually go ham, you can get pretty far pretty fast
- you can talk to models in base-64 and itll respond perfectly like normal. wtf??? why does this happen
- automated interp: your models can be deterministic. your gpt-6 can have say billions of features and you can have a bunch of smaller models tweaking inputs and outputs seeing when the features fire and trying to figure out which what the features correspond to. this sounds promising 👀
- current interp work is taking the activated vectors (logits-y?) and finding features through that, but the end goal would be not even running the model through the activations but being able to learn about the model purely by looking at the weights (very hard)
- research project: find the specialization in the mixtral model