---
layout: single
title: "AI-Derived: Round-robin CCZ is All You Need"
date: 2026-06-16
author_profile: false
permalink: /blog/round-robin-ccz/
---

After much procrastination, I am starting a blog with a fun AI-derived observation. Here is a note, the abstract says it all: [Round-robin CCZ is All You Need](/files/Notes/Round-robin-CCZ.pdf).

This observation, as with many fun things, came from a discussion I had with [Ted Yoder](https://scholar.google.com/citations?user=OhiKBrsAAAAJ&hl=en), when we were trying to learn these cup-product conditions that give logical CCZ gates. 
We didn't make much progress as we got distracted by these round-robin circuits, which were introduced by Ted, Ryuji Takagi and Ike in a [paper](https://arxiv.org/abs/1603.03948) back in 2016 (by the measure of the field of QEC, 2016 is a really, really long time ago). These circuits are really simple. Consider two sets of qubits, $$A$$ and $$B$$. The round-robin CZ gate between $$A, B$$ is the circuit

$$
    \text{CZ}(A,B) = \prod_{(a, b)\in A\times B}\text{CZ}(a, b).
$$

Simple enough. Two interesting facts about these circuits:
- If both $$A,B$$ are support of $$Z$$ logical operators in a CSS code, then $$\text{CZ}(A,B)$$ implements a logical CZ gate between the two logical qubits.
- If either of $$A,B$$ is the support of a $$Z$$ stabilizer, then $$\text{CZ}(A,B)$$ is a logical identity. 

These facts generalize to $$\text{C}^r\text{Z}$$, with any number of controls. Obviously, these circuits are high-depth and very-not-fault-tolerant by themselves. They look nothing like the transversal CCZ circuits people love and work hard for. 

Well, the observation is that these circuits (where all sets are $$Z$$ logicals or at least one is $$Z$$ stabilizer) generate all logical CCZ circuits (transversal, addressable, parallel, whatever). We hypothesized this, and were a little skeptical. We then asked ChatGPT to show this, and dropped the thread after the notation got too hard to parse. At that time, it was yet unclear how much one should trust AI-generated math. 

After OpenAI announced that their model [disproved the long-standing unit-distance conjecture](https://openai.com/index/model-disproves-discrete-geometry-conjecture/), I decided to try this again with Claude Opus 4.8. It produced a proof with heavy notations, which upon checking looks correct. 
This is when my brain reminded me that my good friend and cohort at MIT, [Yuanjie (Collin) Ren](https://collinyuanjieren.com/), had cofounded an AI auto-formalization company called [MerLean](https://arthurmerlean.com/), and he has asked me for prompts to try it on. So I sent the proof to him, and six hours later he sent me an AI-assisted verification of the proof in Lean 4. 

For those of you who haven't used Lean 4 before (I certainly had not): 
- just because something is 'verified in Lean 4' does not make it correct;
- Lean 4 output by itself is a pain to read. But at this point I am too deep down the rabbit hole.

To elaborate on the first point: to prove things in Lean, you give it assumptions and try to deduce conclusions. If your assumptions are wrong, your conclusions are wrong too (if pigs can fly then the universe is a glazed donut). The output I received from MerLean (well, MerLean's disciple Collin), however, had no assumptions. Collin assured me that they had built up a QEC library, where all the assumptions needed for our statement have been proved. So, assuming their library has no bugs, this observation is Lean-verified. 
But the proof (from Claude) was too notation-heavy and a pain to work with. 

So I complained to Claude: "this is too rough to be posted publicly", I said, "please write a self-contained research note intended for publication". Claude was happy: "This is the right next step", it replied, before grinding away. 
In about 20 minutes, it came back with a first draft of this note. The English writing was terrible, but the proof was new and much cleaner. Upon checking, the proof looks correct. I then sent the output to friend and local-CCZ-expert [Varun Menon](https://scholar.google.com/citations?user=SMoAxkcAAAAJ&hl=en), after which us three drafted this note together with much back-and-forth with Claude. 

Now some disclaimers: this observation is not deep; it is at the level of a homework problem for a graduate-level course. If you were aware of this already or if this is known before, please let me know and I'll make sure the references reflect proper credits. In all seriousness, I hope I did not accidentally scoop anyone. 
However, upon checking with several experts on CCZ gates, none of them were aware of this equivalence. [A certain expert](https://lgolowich.github.io/) in fact looked very disturbed by this observation. So I am declaring this operation a massive success in terms of [sniping](https://xkcd.com/356/) friends and being a fun exercise in itself. 

More seriously, it would be interesting to see how AI will continue to transform our work. In this case, we proposed a bite-sized idea and Claude carried it through. In much bigger cases, such as OpenAI’s model’s solution to the unit-distance conjecture, AI established a significant result with excellent execution. 
Is asking the right questions our distinguishing strength? How about interpreting and narrating the ideas? Will AI catch up to that too? I am still optimistic about the future of human scientists and the importance of human intelligence in scientific work. But there is no doubt that our mode of work is changing rapidly.

Finally, an advertisement for MerLean: they are very open to industrial, business and academic collaborations. If you are interested in getting your results Lean-verified, please reach out to Collin (yuanjie@mit.edu). I sure hope that they won't make us obsolete. 
