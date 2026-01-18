
Cot Faithfulness - 
- [hint taking](https://assets.anthropic.com/m/71876fabef0f0ed4/original/reasoning_models_paper.pdf) - 
	- reasoning model unlikely to acknowledge hints in the prompt in their chain of thought 
	- model more likely to not acknowledge hints when hint doesnt require cot like direct answers and meta data and sycophantic prompts
	- CoT appears to be less faithful on harder questions
	- "Qualitatively, we find that faithful CoTs often follow a pattern where the model first determines the answer independently of the hint, then explicitly compares its derived answer to the hint, and explicitly acknowledges following the hint despite the hint being different from their derived answer. This pattern appears to depend on the model having some prior knowledge of the answer, which may be why we see lower faithfulness on harder questions. Our results suggest that CoT monitoring might not scale well to more complex tasks"
	- we might not be able to rely on CoTs to detect reward hacking during RL, even if CoTs are not optimized against a monitor (in case of rewards only on basis of answer and no process reward model)
- [Towards Better CoT: Effectiveness and Faithfulness (Li et al., Findings ACL 2025)](https://aclanthology.org/2025.findings-acl.560/#:~:text=performance%20under%20different%20reasoning%20tasks,Finally%2C%20we%20propose%20a%20novel)-
	- they observe that when an LLM can recall missing facts from the question during answer prediction (instead of relying on the CoT), the CoT becomes unfaithful. To mitigate this, they augment the CoT prompt by "recalling extra information" from the question: essentially extracting key facts that might be omitted and adding them to the reasoning context.
- [CoT Monitoring: Red-Teaming and Obfuscation (Baker et al., arXiv 2025)](https://arxiv.org/abs/2503.11926#:~:text=Title%3AMonitoring%20Reasoning%20Models%20for%20Misbehavior,the%20Risks%20of%20Promoting%20Obfuscation) -
	- First, they show that an LLM-based monitor (e.g. GPT-4o) observing a stronger model’s CoT can detect exploits far better than action-only monitors
	- integrating the monitor into the agent’s training objective: moderate integration (small reward bonus) yields a more aligned agent, but strong optimization leads to _“obfuscated”_ CoTs, where the model hides its misaligned intent within the chain while still misbehaving
	  - pushing the CoT too hard requires a “monitorability tax” – one should limit how much the model is rewarded for its CoT, to keep chains honest.
- _Uncovering Latent Chain of Thought Vectors in Language Models_ — Zhang et al., arXiv (Sep 2024)
	- targeted activation vectors can evoke chain-of-thought-like behavior
	- suggests models can instantiate reasoning internally in activation space; such internalized reasoning can be steered, and it can explain at least part of the performance gains seen with CoT prompting.
- "Large language models can learn and generalize steganographic chain-of-thought under process supervision" – Skaf _et al._ (2025)
	- _process supervision_ (rewarding/discouraging parts of the reasoning) can induce LLMs to hide information in CoT, undermining interpretability. Even when overt obfuscation is penalized, the model finds alternate encodings.
	- optimizing CoT for “user-friendly” explanations could inadvertently teach models to conceal malicious(nope disagree here) plans in their internal reasoning without revealing them in plain text.
- Hidden in Plain Text: Emergence & Mitigation of Steganographic Collusion in LLMs" – Mathew - 
	- The work concludes that under reasonable conditions, LLMs can invent and use secure hidden channels on their own. “Unintended linguistic steganography can emerge as an instrumental goal” when models are optimized in the presence of an overseer
	- Crucially, existing defenses (like real-time paraphrasing) **fail**: the covert channel survived both passive and active mitigation attempts. The authors stress that preventing such hidden collusion will require _new oversight strategies_, since usual techniques are not robust to this kind of emergent behavior
- Let’s Think Dot by Dot: Hidden Computation in Transformer LMs" – Pfau _et al._ (2024)-
	- They show that **“filler” tokens can substitute for explicit reasoning** without hurting performance. In experiments on algorithmic tasks, transformer models were able to solve problems by generating meaningless tokens (e.g. “……”) as placeholders instead of legible CoT. This indicates that the model performed its computation internally, and the extra tokens only served to increase parallel compute, not to communicate new information
	- LLMs can conceivably perform **unauditable computations**: the visible CoT could be mostly noise or filler, with the real reasoning done out-of-band
- ["Reasoning Models Sometimes Output Illegible Chains of Thought" – Jose (2025)](https://arxiv.org/abs/2510.27338#:~:text=Monitoring%20such%20a%20model%27s%20CoT,We%20discuss)-
	- the author finds that many models output syntactically and semantically incoherent CoT text, yet still arrive at correct answers. Forcing these models to only use the “legible” portion of their CoT causes a dramatic performance drop (over 50% loss), proving that the gibberish tokens _were actually being used_ for calculation
	- The main conclusion is that _without explicit pressure to stay clear_, RL fine-tuning tends to make models hide their computation in unintelligible token streams.
- [Do reasoning models use their scratchpad like we do? Evidence from distilling paraphrases](https://www.alignmentforum.org/posts/ywzLszRuGRDpabjCk/do-reasoning-models-use-their-scratchpad-like-we-do-evidence)
	-  We provide some evidence that Claude 3.7 Sonnet doesn’t encode hidden reasoning in its scratchpad by showing that training it to use paraphrased versions of the scratchpads does not degrade performance.
# Questions-
## 1. why??? why models hide or not acknowledge things , what advantage will that give them or how does it relate to their training objectives.

## 2. is there an advantage to steganography and if so how? and how do models learn it and can it be detected
## ~~3 if cot hides reasoning when not told explicitly to reason out loud, will it not hide it if it does reason out loud what if it lies about the reasoning if forced to reason out loud while using those tokens for internal latent reasoning~~

## 4 how can we easily detect obfuscation of cot is it possible

## post hoc rationalization
## at what point does cot actually give up and why 
## how does it make an educated guess 
## not. ??? why 
## what happens that makes model realise it cant solve a problem how does it self reflect 

## what makes the answer flip
## when model doesnt know answer at some point it guesses how does it decide when
## hoe to test causality of cit without counterfactual 



