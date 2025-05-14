+++
date = '2025-05-14T00:00:00-08:00'
draft = false
title = 'LLMs are Making Me Dumber'
+++

Here are some ways I use LLMs that I think are making me dumber:
- When I want to build a Chrome extension for personal use, instead of actually learning and writing the JavaScript, I Claude-Code the whole thing in a couple of hours without writing a single line of code. 
Instead of taking the usual route which would leave me with more actual familiarity with JavaScript, I now shortcut the process leaving me with barely any JS knowledge despite numerous functioning applications.
- When I need math homework done fast, I feed in the relevant textbook pages in context, dump my problems into o3/Gemini, and check its answers for sanity instead of doing the problems myself. I cram before tests. (Yes, this is morally dubious and terrible for learning.)
- When I need to write an email, I often bullet-point what I want to write and ask the LLM to write out a coherent, cordial email. I’ve gotten worse at writing emails.
- My first response to most problems is to ask an LLM, and this might atrophy my ability to come up with better solutions since my starting point is already in the LLM-solution space. 

These are all deliberate trade-offs I make for the sake of output speed. By sacrificing depth in my learning, I can produce substantially more work. I’m unsure if I’m at the correct balance between output quantity and depth of learning. 
This uncertainty is mainly fueled by a sense of urgency due to rapidly improving AI models.
I don’t have time to learn everything deeply. I love learning, but given current trends, I want to maximize immediate output. I’m sacrificing some learning in classes for more time doing outside work. From a teacher’s perspective, this is obviously bad, but from my subjective standpoint, it’s unclear.

Before the rise of LLMs, learning was a prerequisite for output. Learning by building projects has always been the best way to improve at coding, but now, you can build without knowing all the details in the usual sense. Many interesting and valuable projects are doable by LLMs with my hand-holding. There’s so much low-hanging fruit that execution seems much more of a bottleneck than deep understanding and innovation.

However, I might be deluded as the tasks I’m doing are easy and in-distribution. If you do work at the very frontier, LLMs definitely aren’t as helpful and, for very good programmers, their use of these models for coding is [fundamentally different](https://simonwillison.net/2025/Mar/19/vibe-coding/). The question is how this plays out for junior engineers within the 3-5 year time frame. What do I do if LLMs are getting better at coding faster than me? I feel like Kasparov playing Deep Blue for the first time. 

Claude-Code, o3, and Gemini 2.5-pro are extremely good. I can vibe-code full apps without knowing the language I’m writing in. I just need a good high-level understanding of the code and steer Claude when necessary. The key question is: Can you learn this high-level steering without having written a lot of the code yourself? Can you be a good SWE manager without going through the SWE work? As models become as competent as junior (and soon senior) engineers, does everyone become a manager?

The argument against “offloading learning to do things” is that I will soon hit a barrier and be unable to do anything new, as the LLMs limit my ability. 

When vibe-coding, I’m essentially a wrapper around these models, providing the ability to take actions on a computer and some high-level coherence. Models will soon obtain these skills as well. Am I using the model as an assistant, or is it the other way around?

## Historical Analogies:
- Calculators. People used to calculate logarithms by hand and entire careers would be spent doing calculations that can be done in <1 ms on a modern calculator. No one lamented the advent of calculators. It’s a perfect example of offloading menial work, allowing humans to spend more time on the interesting things. One distinguishing factor about this situation is that everyone still needs to learn arithmetic. We don’t say “don’t learn arithmetic! Calculators can do that already. Just go do algebra!” even though many influential people in AI do say you shouldn’t learn coding in the usual sense. You need arithmetic to do everything after. This analogy argues for “write 100,000 lines of code yourself before you start extensively using LLMs.” While calculators have automated away long calculations, we can still perform these calculations by hand if we needed to. However, I wouldn’t be able to write those lines of JavaScript manually. It’s a different level of abstraction.
- GPS. It’s so reliable that I’m fine being unable to navigate. 
I’ve never gotten in a situation where I wish I had learned to navigate without Google Maps beforehand. 
But this is also a narrow skill that isn't foundational to other higher-order ones. 
Maybe software engineering will be something as obsolete as navigating where you can wholly offload it? However, that seems unlikely given the difference in complexity of the two tasks.
- Printing press / Typing. People thought that when computers and typing became popularized, people would stop writing and it would deteriorate their thinking ability. People used to copy and scribe everything by hand to ingrain it in memory, and yes, that might be better than retention compared to typing, but the sheer speed typing provides overrides that.
- Industrial Revolution. A significant portion of menial labor was no longer needed from humans. Again, the skills that were automated here wasn’t foundational to other disciplines and could be boxed up neatly. The issue is that the skills being threatened are significantly larger in this AI situation. It’s intelligence. What’s next? Labor -> intelligence -> ?
- Chess. In 1996, a computer system, DeepBlue, beat Kasparov, the world chess champion, for the first time in history. 
By 2005, chess engines were better off without any human intervention. 
Seven years (1998-2005) was the short-lived period when human + engine (centaur chess) was better than engine. Human + AI will not always be better than AI itself. 
However, chess is a closed, fully-contained system, unlike programming and problem-solving which are more open-ended.
**We have now entered the centaur age for programming. But how long will this collaboration last?** 
- Assembly to C to Python. Almost no one writes assembly by hand anymore (unless you work at Deepseek) and this is good. Our output increases drastically because compilers do all low-level work for us! While CS undergrads are still required to take classes on assembly, most productive SWEs never interact with assembly. Moving up the ladder of abstraction has consistently been good. 

Looking at historical examples, successful cases of offloading occurred because the skills are either easily contained (navigation) or we still know how to perform the tasks manually but simply don’t need to anymore (calculator). The difference this time is that intelligence cannot easily be confined. 

# Arguments against LLMs:
- I’m just a LLM wrapper. 
- I’m fully betting on models hitting inflection very soon, and if they don’t, I will completely stagnate.
- In the tortoise and hare analogy, I’m the hare, getting small wins, but losing the overarching race.
- Even if models get good fast, I’ll have no moat after. I’m just maxing my output until models get agency + long-term coherence.
- I won’t be able to do any “novel work”.

# Arguments for LLMs:
- I will ~5x my output in the short term. (This will vary a lot depending on the specific person, but I think this factor is very high for me given my baseline isn’t as high as 10-year SWEs)
- I snooze I lose. Sure, I’ll have no moat after, but at least I’ll get something done in the next five years. No one knows what happens after.
- I sure as hell want to be the hare if the race is going to be short.
# One-on-One Tutors

Using these models as tutors to supercharge learning and speed up output is a potential balance between the two extremes. [Bloom's two sigma effect](https://en.wikipedia.org/wiki/Bloom%27s_2_sigma_problem) is the big sell.

They’ll explain questions I have about the math concepts instead of doing my homework.
They’ll nudge me to where the bug is and I’ll make the change myself instead of tabbing.

This is the dream use case of LLMs for teachers. You add scaffolding so that instead of following all your instructions, it acts as a teacher would, rejecting requests that are harmful for learning (obviously you can already do this but discipline isn't scalable). Obligatory who’s building the Cursor for tutoring?

However, grinding out the repetitive tasks is also what ingrains these skills into your system 1. A similar analogy holds for LLMs themselves: a model that internalizes and manipulates information at a latent level is fundamentally different from one that manipulates retrieved information at the token level. The same goes for humans. When applying a theorem for the first time, I have to decompose each part and operate each part in my mind separately. Mathematicians batch multiple theorems into a single conceptual unit, allowing them to process more complex ideas. It’s [*the Magical Number Seven, Plus or Minus Two*](https://psychclassics.yorku.ca/Miller/). To learn the content, you must go through the motions yourself. You can’t abstract it away. 

[Derek](https://www.youtube.com/watch?v=0xS68sl2D70) says that AI will not finally revolutionize and solve education. 
It’ll change it in numerous ways, but it won’t be the big thing everyone has been waiting for. Learning by yourself with o3 as a tutor is amazing, but for the average student, other factors such as motivation, structure, and companionship, outweigh this. 
Yes, this will allow the top 5% instead of the top 0.5% of students to experience the 2-sigma effect, but the education system is built for the average student. 
This is why lecture formats haven’t changed in the last hundred years. It’s just the best way to learn based on educational research. 

Will we have to completely outlaw AI until some stage of education? Probably, but I’m optimistic that, with good scaffolding and intentionality, an empowering tutor for learning can benefit everyone. Lots of small details need to be perfect for this product to be good.

However... even this might still be too slow. Why understand every line of code deeply if you can just build and ship? Even this optimal case as one-on-one tutors is a tradeoff that might not be worth it. 

# Finding Balance 

Total offloading cripples true learning but maximizes short-term speed and output, and finding the right balance is crucial. 

For me, this looks like relentlessly automating and vibe-coding small experiments within the models' capabilities, but being more wary of leaky abstractions and understanding every line of code I’m pushing for larger projects.

Inevitably, parts of my brain will degenerate and fade away, so I need to consciously decide what I want to preserve or my entire brain will be gone. What skills am I NOT okay with offloading? What do I want to do myself?

- I’m not okay with being unable to think for myself. I want to retain my ability to reason from first principles and develop novel ideas. 
    - Block out time every day to write without LLMs.
    - Have long conversations with friends who push back on my ideas.
- I’m not okay with being unable to make decisions. I want to take responsibility for my actions. 
    - Work on large, meaningful projects.
- I’m not okay with being unable to do long-term tasks. I want to read books without being distracted and work on things that span months to years.
    - Read books.
    - Work on large, meaningful projects.

Thanks for Jason, Femi, Miles, Gemini, GPT-4.5 and more for feedback.

## Relevant reads:

[brAIn drAIn by Erik Hoel](https://www.theintrinsicperspective.com/p/brain-drain)

[Thoughts on Cursor by Me](https://vvvincent.me/thoughts-on-cursor/)

[The Problem with Vibe Coding by Dylan Beattie](https://dylanbeattie.net/2025/04/11/the-problem-with-vibe-coding.html)

[What Everyone Gets Wrong About AI and Learning by Derek Muller](https://www.youtube.com/watch?v=0xS68sl2D70)

[The Whispering Earring by Scott Alexander](https://gwern.net/doc/fiction/science-fiction/2012-10-03-yvain-thewhisperingearring.html)

[Not all AI-assisted programming is vibe coding by Simon Willison](https://simonwillison.net/2025/Mar/19/vibe-coding/)
