### **Month 1: Learning the Ropes & Foundational Concepts**

**Overview Checklist for Month 1:**
- [x] Understand the high-level architecture and data flow of a GPT-style transformer.
- [x] Define core mech interp terms like superposition, polysemanticity, features, and circuits.
- [ ] Gain a practical understanding of key techniques: activation patching, probing, and using SAEs.
- [ ] Become proficient in using the basic functionalities of TransformerLens or nnsight for running models and accessing activations.
- [ ] Internalize the strategic frameworks for conducting research proposed by Nanda and Steinhardt.

---

#### **Weekly Checklists for Month 1**

**Week 1: Core Concepts & Transformer Basics**
*   [x] **Read:** "A Mathematical Framework for Transformer Circuits" to understand the core components like the residual stream and attention heads.
*   [ ] **Read:** Neel Nanda's "Comprehensive Mechanistic Interpretability Explainer & Glossary" sections on General Concepts, Representations, and Superposition.
*   [ ] **Watch:** 3Blue1Brown's "Essence of Linear Algebra" series to solidify your understanding of vectors, matrices, and basis changes.
*   [ ] **Self-Test:** Explain the purpose of the residual stream, attention heads, and MLP layers to yourself or a peer. Use an LLM to check your understanding.

**✅ Week 2: Essential Techniques**
*   [ ] **Read:** The "Activation Patching" section of Ferrando et al.'s survey and Nanda's glossary. Understand it as a method for causal intervention.
*   [ ] **Read:** The "Probing" section of Ferrando et al.'s survey. Understand its use for detecting information and its limitations (correlation vs. causation).
*   [ ] **Read:** The "Sparse Autoencoders (SAEs)" sections in Nanda's paper list and Ferrando et al.'s survey to learn how they help find features in superposition.
*   [ ] **Self-Test:** For each of the three techniques (patching, probing, SAEs), write a one-paragraph summary of what it does, what question it answers, and one potential pitfall.

**✅ Week 3: Tooling & Hands-On Practice**
*   [ ] **Install:** TransformerLens and nnsight libraries.
*   [ ] **Complete:** The ARENA tutorial "Introduction to Mech Interp & TransformerLens". Focus on loading models, running them with hooks, and caching activations.
*   [ ] **Complete:** The ARENA tutorial "Indirect Object Identification (IOI) Circuit Analysis". This will give you hands-on practice with activation patching.
*   [ ] **Explore:** The basic tutorials for nnsight to understand its syntax for accessing and intervening on model internals.

**✅ Week 4: Understanding the Research Process**
*   [ ] **Read:** Neel Nanda's blog post "How I Think About My Research Process: Explore, Understand, Distill".
*   [ ] **Read:** Jacob Steinhardt's blog post "Research as a Stochastic Decision Process". Pay attention to the concepts of prioritizing by information rate and de-risking.
*   [ ] **Synthesize:** Write a short plan for a hypothetical 1-week mini-project, outlining what you would do in the "Explore," "Understand," and "Distill" phases.
*   [ ] **Plan:** Brainstorm 3-5 potential mini-projects for Month 2 based on your readings. Examples: Replicate a small part of the IOI circuit, or test a specific head's function in GPT-2.

---

### **Months 2 & 3: Practicing Research & Deepening Skills**

**Overview Checklist for Months 2 & 3:**
- [ ] Complete at least 4-6 short (1-2 week) research sprints.
- [ ] Practice the full research cycle: form a hypothesis, design and run experiments, analyze results, and summarize findings.
- [ ] Move from replicating results to extending them in small, novel ways (e.g., trying a technique on a different model or prompt distribution).
- [ ] Become comfortable with debugging unexpected experimental results.
- [ ] Begin writing up your findings, even if just in private documents, to practice distillation and communication.

---

#### **Weekly Checklists for Months 2 & 3 (Example Sprint Cycle)**

This is a template you can repeat. A "sprint" could last one or two weeks.

**✅ Week 5: Sprint 1 - Planning & Exploration**
*   [ ] **Select Project:** Choose one of the mini-projects you brainstormed. A good first choice is replicating a known result, like identifying the name-mover heads from the IOI paper.
*   [ ] **Explore:** Run the model on relevant prompts and visualize activations. Use techniques like direct logit attribution and attention pattern visualization to gain initial insights and form a concrete hypothesis.
*   [ ] **Log Everything:** Keep a detailed research log of your experiments, observations, and ideas.

**✅ Week 6: Sprint 1 - Understanding & Distillation**
*   [ ] **Test Hypothesis:** Design and run activation patching experiments to causally test your hypothesis.
*   [ ] **Analyze:** Interpret your results. Do they support your hypothesis? What are the limitations?
*   [ ] **Summarize:** Write a short (1-2 page) summary of your project, including your hypothesis, methods, results, and conclusions. This is a crucial step for the "Distill" phase.
*   [ ] **Post-Mortem:** Reflect on the sprint. What went well? What was challenging? What skills do you need to improve?

**✅ Weeks 7-12: Sprints 2-4**
*   [ ] **Repeat:** Follow the Plan -> Execute -> Reflect cycle for new mini-projects.
*   [ ] **Increase Scope:** Gradually increase the complexity of your projects. For example:
    *   **Sprint 2:** Extend the IOI analysis to a different set of names or sentence structures.
    *   **Sprint 3:** Try to create a simple steering vector (e.g., for sentiment) and test its effect.
    *   **Sprint 4:** Investigate a weird behavior you noticed in a model, forming your own hypothesis from scratch.

---

### **Month 4: Full Research Project & Communication**

**Overview Checklist for Month 4:**
- [ ] Select and complete a single, more ambitious research project that takes 3-4 weeks.
- [ ] Practice rigorous experimental design, including the use of strong baselines and ablations.
- [ ] Produce a polished public-facing output (e.g., a blog post, conference-style paper, or detailed Colab notebook).
- [ ] Seek feedback on your work from peers or mentors.

---

#### **Weekly Checklists for Month 4**

**✅ Week 13: Project Ideation & Planning**
*   [ ] **Brainstorm:** Generate several potential project ideas. Use your experience from the mini-projects to gauge what is feasible and interesting.
*   [ ] **Evaluate:** For your top 2-3 ideas, write a one-page proposal outlining the research question, proposed methods, and expected outcomes.
*   [ ] **Select:** Choose the most promising project and create a detailed plan with weekly goals.

**✅ Weeks 14-15: Execution & Analysis**
*   [ ] **Execute Plan:** Carry out the experiments outlined in your plan. Be prepared to adapt as you get results.
*   [ ] **Deeper Analysis:** Go beyond surface-level results. Red-team your own conclusions, consider alternative explanations, and run additional experiments to strengthen your claims.
*   [ ] **Start Writing:** Begin writing up your methods and results as you go. Don't leave this until the end.

**✅ Week 16: Distillation, Write-up, and Sharing**
*   [ ] **Finalize Results:** Complete any final experiments and create clear, compelling visualizations for your key findings.
*   [ ] **Write Full Draft:** Write a complete draft of your paper or blog post. Focus on crafting a clear narrative that tells the story of your research.
*   [ ] **Get Feedback:** Share your draft with peers or a mentor and incorporate their feedback.
*   [ ] **Publish:** Post your work publicly (e.g., on a personal blog, LessWrong, or arXiv). Congratulations


