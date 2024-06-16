## Copy paste directly from article chapter 1
In addition to insider bullishness, I think there’s a strong intuitive case for why it should be possible to find ways to train models with much better sample efficiency (algorithmic improvements that let them learn more from limited data). Consider how you or I would learn from a really dense math textbook: 

What a modern LLM does during training is, essentially, very very quickly skim the textbook, the words just flying by, not spending much brain power on it.  
Rather, when you or I read that math textbook, we read a couple pages slowly; then have an internal monologue about the material in our heads and talk about it with a few study-buddies; read another page or two; then try some practice problems, fail, try them again in a different way, get some feedback on those problems, try again until we get a problem right; and so on, until eventually the material “clicks.” 
You or I also wouldn’t learn much at all from a pass through a dense math textbook if all we could do was breeze through it like LLMs.
But perhaps, then, there are ways to incorporate aspects of how humans would digest a dense math textbook to let the models learn much more from limited data. In a simplified sense, this sort of thing—having an internal monologue about material, having a discussion with a study-buddy, trying and failing at problems until it clicks—is what many synthetic data/self-play/RL approaches are trying to do.

Major breakthroughs are in RLHF and variants, chain of thought reasoning to solve math & SWE problems (walking through the steps until the answer is achieved works better because it enables more useful information flow each token gen / forward pass, scaffolding -> a bunch of specialized models solving a problem in few-shot settings rather than GPT-4 figuring it out the first try. Far less compute used from this last approach and enabled more capabilies when we optimize it further. tokenization hacks -> query tools like calculators. more compute efficient algos provides us with longer ctx length. really hard evals lead us to unconventional thinking which lead us to non-trivial answers that would otherwise be far out.

## Features for the futures:
- working memory/replay buffer to store long term relationships/dependencies about a client's needs
- recurrent architectures to digest a problem thoroughly instead of dumbly producing the next token based on how a bunch of internal features attended to one another. could use a a scaffolding variant here but having an architectural change might scale better. optimize for longer-horizon problems. 
- a good research project would be looking at how many useful "attentions" (the spectrum of useful attending of tokens/features attending to others) in each layer. connect this to other hyperparameters and  architectural changes to see what we can add/change about the base self-attention algorithm to get more usefulness out of all its parameters. 
- system 1 & 2 rather than just system 1.
- 


## Threats:
- the central problem here is security rather than
unpredictability/exploitability of the largest models
- … Is this what we see at OpenAI or any other American AI lab? No. In fact,
what we see is the opposite — the security equivalent of swiss cheese. Chinese
penetration of these labs would be trivially easy using any number of industrial
espionage methods, such as simply bribing the cleaning crew to stick USB dongles
into laptops. My own assumption is that all such American AI labs are fully
penetrated and that China is getting nightly downloads of all American AI
research and code RIGHT NOW…  -> Marc Andreessen
- obvious but good to remind ourselves about protecting model weights (the
destination) & the algorithmic secrets required to obtain the end weights via
pretraining, finetuning, RLHF, etc
- CCP gaining advantage of holding the technology that allows them to keep up
via automation, all through espionage
- not only would it present a national security risk but being in a
superintelligence race (naive: whoever gains it first gets absolute control over
the other (agi in a box problem)) but it means little to no margin of safety in
development of these systems. this means the mech interp techniques would need
to improve a lot in order to understand potentially dangerous internal behavior


### Random Notes:
- Best to think in OOMs (orders of magnitude) rather than 2x, 6x, 13x, etc.
- Sure, recursively improving general intelligence or whatever people call it. I'd like to question the takeoff speed and practicality here. The # of agents doing the research to improve themselves would cost an amount per agent or per task. This would be an exponential takeoff with a very explicit limit -> cost, energy, & climate. Having an agent smart enough to test would take a while to actually build & test. Assuming this is autoregressive, it would fail a lot at generating useful code and having the creativity we humans do. You would need to smartest people in the world giving feedback constantly. Leopold has strictly stuck to the obvious advancements (were the hype is at) in AI so having this expected high quality data with some sort of RLHF mechanism to teach a model to build itself would take a while to implement and scale. Not out of possibility but there will surely be some missing pieces here holding us back from the pot of gold. 
- we only have a limited amount of data from existing trained models but people  mainly compare GPT-2 to GPT-4 in terms of performance change over time. we need to understand whats going on under the hood to drawn such concise general intelligence predictions.  
- there needs to be clear instructions on how to actually conduct AI research. 
- It could be possible that without knowing, leopold hand picked examples to
make all this progress seems like it "just around the corner" when there are
other challenges and really hard problems in edge cases
- aluminum smelting companies for the energy requirements handling the compute
requirements this decade. could buy into the ETFs supporting energy
infrastructure (look into advancements in the field to see where most
infrastructural growth will occur)
- since building up powerplants and giga clusters in other parts of the world
could be faster, we have to consider the influence they have over research in
the US. they can peek into the weights or training run at any point if they are
careful enough and this poses a national security risk. this then jumps to a
climate issue if we keep energy + cluster development in the US due to pollution
from our #1 energy source of gasoline power plants
- might be smarter for long-term personal financial investment in compute
manufacturing (UV lithography) / energy bottlenecks because research and
innovation will kick that right out of place leaving massive gains for those
early invested 
- since you have a national security threat, all the top end research would fall
  into the hands of military and government control, siphoning power from the
  secretive private companies. I wonder if really good corp structure could
resolve some of this.
- its healthy to consider the possible capability limitations of hacks like FP8
  quantization could force the model to learn to adapt around low precision
and thus prevent it from focusing more parameters on the proclaimed
"intelligence" part of the model. we may discover that the true issues lay at
the maximally useful weights in the neural net
- I have heard from a number of researchers that the research conducted in big
tech is often "compute limited". I don't why a single consumer grade GPU or even
an A100 isn't enough for a ton of algorithmic progress. Of course the scaling
experiments require more compute but the base hacks like layernorm and residual
connections can be reproduced on many scales w/ 4GB of VRAM.
- scaling laws essentially says you can determine the exact loss to a very high
  precision based on the total training tokens and model size (VRAM & data
amount (assuming a quality threshold))
- 


## Other Resources
- GPT scaling laws (chinchilla) -> https://arxiv.org/pdf/2203.15556
- original scaling laws w/ dario amodei -> https://arxiv.org/pdf/2001.08361
- super thorough scaling paper I probably won't read -> https://arxiv.org/pdf/2112.11446
