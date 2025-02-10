---
layout: post
title:  "Podcast Notes"
date:   2024-07-28
---

# Dylan, Nathan on Lex

- top labs all all have their own crawlers
- quality of data is crazy underrated
- v3's main differences: MLA, MoEs
- Deepseek went below C to assembly-level coding for communications engineering stuff
- v3 has 256 experts. other models only have ~32. v3 is muchhh more sparse. 
this sparsity leads to some gpus sitting idle a lot since some experts are used less
they use auxiliary loss during trianing so all experts are used
- r/microwavegang caused loss spikes LMAO
- it's not luck. there are improvements you can make in so many places
- quant uses a lot of nlp too? processing news articles and whatnot
- once models get good at long-horizon tasks, spending most of your compute on inference makes a lot of sense
- misinformation spread due to LLMs was a smaller problem than ppl thought it would be (AI Snake Oil)
- ai capabilities will have an overhead time period where the limiting factor is that they can't be deployed at scale. they won't be limited by capability
- china's infra, datacenter, power capacity is not even comparable to the US's
- china will win in the long-term if AI doesn't change the world in less than 10 years. they will get their own superior chips, have better production, have more energy and mog.
- "if ai takes a long time to become differentiated, we've decapped the financial performance of american companies" wait i'm not sure how much i buy this. is this because of export controls? 
you're telling me that china wouldn't have gone full send on making chips if not for these export controls?
- china at the top level hasn't become totally scale-pilled yet. they haven't committed hard like the US
- deepseek might be the start of a cold war-esque dynamics
- an angle for chinese taiwan invasion: "if we can't get access to the chips, no one else should be able to". if tsmc dying hurts others more than themselves, it would make sense.

- who's talking about reverse moore's law? halving the cost of chips every 18 months means doubling the cost of fabs every 18 months. i think the actualy numbers are more like 1.5x more expensive 

- nvidia is the only semiconductor chips that has never had a fab
- export controls is a clear sign that US does not want to "work with" China on AI. they want to keep this tech in their control by all means possible
- further instability coming?
- the world has historically been more peaceful when there is one superpower
- three axes to think about chips: FLOPS, memory bandwidth, interconnect
- why is deepseek so fucking cheap? their MLA is a substantial architectural innovation to attention, making memory usage 80-90% less. the attention is still quadratic though. i assume it's some big constant factor reduction.
- r1 is 27x cheaper than o1 (oai might have priced up a lot)
- oai has 75% gross margins for inference. that's crazy
- alibaba and deepseek aren't close to the chinese government
- race to the top ahh
- "superhuman persuation will come before superintelligence" hmm what does this look like?
- LMAO someone from the gemini team working on long context got poached to Meta which basically means the next Llama will have 1M context length too
- meta's power_plant_no_blow_up operation in pytorch
- what is tranium, amazon's chip
- superclusters are for training. you have all gpus connected by high speed networking. you can do inference in scattered, smaller datacenters.
- why doesn't google sell tpus?
some of tpu design is optimized for google-specific tasks: youtube, search, ...
- aws generates 60+% of amazon's profit. that is crazy. it's only ~15% of the revenue but has much higher margins.
- snapchat was on an exponential growth (quarterly growth rates of 17%) but then instagram introduced stories which led snapchat's growth to flatline. software engineers = snapchat, good ai systems = instagram stories?


# Dario, Amanda, Chris on Lex 

- data just won't be a bottleneck. synthetic data will work.
- $100 billion cluster by 2027
- anthropic's mission is to make AGI go well. they're fine with OpenAI getting there first if it means they do it safely? encouraging other AGI companies to follow safety measures because they'll look bad if Anthropic is doing it but they're not. safe race dynamics lmao
- anthropic's naming scheme is so cool:
haiku (short poem): small, fast, cheap model
sonnet (medium-length poem): medium model
opus (magnum opus, largest piece of work): smartest, biggest, most powerful model
- naming models is really hard lmao
- they do occasional A/B tests before releasing a model
- it is VERY HARD to just change one thing about the model like "make it apologize less". everything is intertwined.

- two main risks: catastrophic misuse, autonomy (model doing bad things itself)
- a uniform standard for the entire industry is needed
- poor regulation is worse than no regulation. if you install bad regulation, it makes everyone conclude that regulation itself must be bad and even when good regulation comes around, there won't be support.

- instead of trying to convince your boss of your vision, just go out and live out the vision. if you're right, your boss will have to follow you later.
- race to the top instead of the bottom. if everyone is copying everyone's good practices, everyone wins

- talent density is more important than talent mass

- open-mindness is super key. curious exploration of looking at things with new eyes
- play with the models!

- it's very possible that post-training will cost more than pre-training in the future
- unhobbling gains from post-training are bigg
- dario believes timelines will happen in 5-10 years over 5-10 hours or 50-100 years
- if you try to please a lot of people, what you produce has to be "average"
- circuits and features are the "proteins, veins" of models. are there organs?
- mech interp engineers live so much better than neuroscientists LMAO
(watched the amanda + chris sections but didn't write much down)

# Dylan and Jon on Dwarkesh (9/10)
- "China has been hacking ASML for five years". wtf huh i gotta read about this 
- china can poach tsmc employees pretty easily
- liang mong song lost a promotion in tsmc and took a shit ton of ppl to samsung (apparently he's not THAT op)
- so much of semiconductor knowledge is passed down "apprentice-master" style 

- china should centralize their compute
- china could build a 10 gigawatt data center in 6 months centered around gorges dam
- there's some aluminum mill in china which is alrd 5+ gigawatts
- packaging
- china was 45% of asml's revenue??
- us sanctions on china chip manufacturing is REALLY complicated
- they can just choke out something like lithography
- Jon doesn't think the us can stop chinese semiconductor from growing
- china could get centralized 1e29 flops training run faster than the us
- china is still using all their chips for like huawei phones
- huawei is so fucking cracked. no tsmc, can't ship to europe, but still outcompete nokia, sony ericsson

- us nationalization vs oai/xai/ant/google/meta fighting separatly

- 2nm is going not going to be viable unless demnad/ai gets much higher
- what does all of this mean man? gotta read up on computers

> When you moved from 90 nanometer to 80 or 70 something, you got 2x. Dennard scaling was still intact. But now when you move from 5 nanometer to 3 nanometer, you don't double density. SRAM doesn't scale at all. Logic does scale, but it's like 30%. All in all, you only save about 20% in power per transistor. But because of data locality and movement of data, you actually get a much larger improvement in power efficiency by moving to the next node than just the individual transistors' power efficiency benefit. For example, if you're multiplying a matrix that's 8,000 by 8,000 by 8,000, you can't fit that all on one chip. But if you could fit more and more, you have to move off chip less, go to memory less, etc. The data locality helps a lot too.

- if china invades taiwan, we will not be thinking about ai. cars, phones, screens, everything using electronics will be fucked

How does one learn about semiconductors?
- there aren't "18 year old dropout turned engineer at openai"s in the semiconductor industry
- everything is so fucking specialized it's harder to break in
- AI is new. all the frontier methods are on the Internet. There is ZERO frontier tech about semiconductors. Everything is locked in labs. Zero documentation online.
- You cannot be full stack. There are literally a thousand layers in the production stack.
- "semiconductor manufacting is the most complicated thing humans do"
- there are humungous innovations still available in architecture. literal 100x gains available

- china destroys us at image recognition

- GPUs/research engineer is your research velocity
- SSI with $1 billion would only be able to run a ~30k GPU cluster. xAI got a 100k cluster running
- other big companies like Google, OpenAI can't do what Elon did because of environmental policies
- dylan expects Google, MSFT to drop their environmental commitments as scaling progresses :skull:
- money split (very rough): 80% gpus, 10% datacenter, 10% power

- there's a gigawatt potential dam in ethiopia??
- gigawatt datacenter in malaysia for bytedance (tiktok)
- 100k GB200 cluster going up in the middle east
- datacenter capacity: US -> China -> malaysia -> middle east -> ...
- OpenAI cluster in Arizona, xAI in Memphis 
- by next year, 300-600k GPU clusters where the GPUs are 2-3x faster
- OpenAI will need 50-100 billion dollars to do this 
- 1e30 run will cost multi-hundred-billion dollars
- Microsoft is taking incredible credit risk

- AGI = God lmao. Pascal's wager. "the cost underinvesting in AI is more than overinvesting
- where is the additional money going to come from? Dylan keeps saying revenue doesn't matter but Jon isn't a believer. GPT-4 cost $500 million to train.
- Dylan sounds like an apostle 

- Even Jon has imposter syndrome
- Dylan goes to fucking 40 conferences a year. Confs on everything in the technical stack

- Memory is a major opportunity 
- Find what you enjoy, work your ass off, profit
- We aren't at the Pareto optimal


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


# Patrick McKenzie on Dwarkesh (7/28)
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


# Sholto Douglas and Trenton Bricken on Dwarkesh (4/16)

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