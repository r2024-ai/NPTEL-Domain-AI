# AI Policies, Regulations, AGI - Part 3

# AI Summer School — Summary Notes

## 1. AI Arms Race & Competition

* AI development is becoming highly competitive, with companies competing on:

  * Model capabilities
  * Compute
  * Parameters
  * Data
  * New model releases
* AI is increasingly viewed as a **revenue-generating business**, not merely a research activity.
* Organizations are investing heavily in AI because they see significant potential to increase AI-related revenue.
* AI adoption cannot be driven only by a central AI/CoE team.

  * Non-technical teams such as **HR, procurement, etc.** need to identify useful business use cases.
  * Therefore, organizations are investing in AI education, training, and awareness across employees.
* The discussion suggested that AI monetization is expected to become increasingly important around **2026**. 

### Important idea

> AI competition is not only about building bigger models; it is also about **democratizing AI and finding useful business applications**.

---

# 2. Will the AI Arms Race Continue?

A key question was whether simply adding:

**More compute + more data → Better models**

will continue indefinitely.

### Scaling laws

The discussion questioned whether AI's current scaling behavior will continue forever.

Possible scenario:

**More compute/data → improving models → eventually diminishing returns or a "wall"**

If scaling eventually stops producing significant improvements, the current AI arms race could slow down.

### Moratorium debate

There have been proposals to temporarily slow AI development.

The speakers expressed skepticism that a complete moratorium would be practical.

Instead, one proposed approach was:

> Continue AI development, but increase investment in **AI safety and responsible AI** alongside model development.

One proposal discussed was approximately:

**10% of AI model-development spending → Responsible/Safe AI**

---

# 3. Democratization of AI

The competition between companies can have a positive side effect:

* Technology becomes cheaper.
* Knowledge becomes more accessible.
* Open-source models become available.
* Smaller models emerge.
* AI becomes less proprietary to a handful of companies.

The discussion mentioned the coexistence of:

* Large Language Models (LLMs)
* Small Language Models (SLMs)
* Open-source models
* Specialized models

### Key takeaway

There may not be one model that dominates every use case.

Different models can be appropriate for different problems.

---

# 4. Don't Use GenAI as a Hammer for Everything

One of the strongest messages in the discussion:

> **Don't use Generative AI simply because it exists.**

Instead:

### Problem → Appropriate technology → Desired outcome

Before choosing GenAI, ask:

1. What is the actual problem?
2. What intervention is required?
3. Can a traditional rule-based system solve it?
4. Can a simple ML model solve it?
5. Does it actually require an LLM/GenAI model?
6. What is the cost and environmental impact?
7. Does the solution actually solve the original problem?

### Example

If a simple ML model can solve a problem, using an expensive GenAI model may create:

* Higher compute cost
* Higher energy consumption
* Higher complexity
* Sustainability problems

This was described metaphorically as **"finding the nail for the hammer."** 

---

# 5. Can AI Be Creative Like Humans?

The discussion explored whether AI can produce creativity comparable to humans.

### Human creativity

Human creativity often comes from:

* Mistakes
* Irregularities
* Asymmetry
* Inconsistencies
* Experience
* Intuition
* Instinct
* Failure
* Unexpected connections

The question was whether AI can reach the same level.

### AI-generated art

AI has already generated artwork that has been commercially valuable.

However, one argument raised was:

> AI may reproduce characteristics of human creativity without necessarily having the **organic experience or intention** behind the creation.

---

# 6. Can AI Think Like Humans?

This was treated as a deeper philosophical question.

There are actually several different questions:

### Question 1

**Can AI think?**

### Question 2

**Can AI think like humans?**

### Question 3

**Can AI have human-like intention, intuition and instinct?**

These aren't necessarily the same.

---

# 7. AI Mistakes vs Human Mistakes

LLMs can:

* Make mistakes
* Hallucinate
* Produce unexpected outputs

But the speakers questioned whether an AI hallucination is equivalent to human creativity.

### Human mistake

A human mistake can arise from:

* Experience
* Intention
* Emotion
* Intuition
* Instinct
* Context

### AI mistake

An AI mistake may arise from:

* Pattern recognition
* Training data
* Probabilistic generation
* Model behavior

Therefore:

> **An AI hallucination should not automatically be considered equivalent to human creativity.**

---

# 8. Next-Token Prediction vs World Models

One view discussed was:

> LLMs are fundamentally doing **next-token prediction**.

Another perspective is that modern multimodal AI goes beyond simple text prediction.

Modern systems can work with:

* Text
* Images
* Audio
* Video

This suggests that increasingly sophisticated AI systems may develop something closer to a **model of the world**, rather than merely predicting the next word/token.

This was presented as a reason for optimism about future generations of AI.

---

# 9. Hallucination — Is It Good or Bad?

An interesting point:

> Some degree of hallucination can contribute to creativity.

But the important question is:

**How much hallucination is acceptable for a particular use case?**

For example:

| Use case              | Hallucination tolerance |
| --------------------- | ----------------------- |
| Creative writing      | Potentially higher      |
| Brainstorming         | Potentially higher      |
| Medical information   | Very low                |
| Financial information | Very low                |
| Enterprise workflows  | Depends on use case     |
| Code generation       | Requires validation     |

So the relevant question isn't simply:

**"Can the model hallucinate?"**

It is:

**"What level of hallucination is acceptable for this application?"**

---

# 10. Data Privacy & Enterprise AI

A major concern from enterprise customers:

> "If I give my data to an AI model, will that data be used for another customer's solution?"

### Proposed enterprise solution

Deploy the model **inside the customer's own infrastructure/environment**.

For example:

**Customer infrastructure → Customer data → Customer-specific AI model**

rather than:

**Customer data → external shared foundation model**

Possible approaches:

* Private infrastructure
* Open-source foundation models
* Customer-specific models
* Small Language Models
* Fine-tuned models

This can help address concerns about sensitive enterprise data leaving the organization's environment.

---

# 11. AI Inclusion & AI Literacy

Another major topic:

### Digital divide → AI divide

Some populations may already have limited:

* Digital literacy
* Smartphone access
* Internet access
* Technical resources

If AI adoption happens unevenly, the existing digital divide could become an **AI divide**.

The UN and other organizations are therefore interested in AI inclusion, particularly in the Global South.

### Important principle

AI should not only benefit:

* Wealthy countries
* Large companies
* Highly educated populations
* Technology professionals

It should also be accessible to underserved populations.

---

# 12. AI & Sustainability

AI requires significant:

* Compute
* GPUs
* Data centers
* Electricity
* Cooling
* Hardware manufacturing
* Silicon/components

Therefore:

> **AI's environmental impact needs to be considered alongside AI development.**

### Possible solutions

#### 1. Smaller models

Use the smallest model capable of solving the problem.

#### 2. CPU instead of GPU

If a model can run effectively on a CPU instead of GPU, energy and infrastructure requirements can be reduced.

#### 3. Edge AI

Move AI computation closer to the user/device.

Example:

**AI assistant running on a laptop → less dependence on large centralized infrastructure.**

#### 4. Model orchestration

Instead of:

**Every task → Large LLM**

Use:

**Simple task → Small model**
**Complex task → Larger model**

#### 5. One-bit Transformers

Research is exploring models capable of running with significantly reduced computational requirements.

---

# 13. AI Can Also Help Solve Energy Problems

The discussion wasn't only about:

**AI → energy consumption**

AI can also help solve:

**Energy → sustainability problems**

Potential applications include:

* Renewable-energy optimization
* Data-center optimization
* Solar/wind utilization
* Energy-aware workload scheduling
* Reducing dependence on traditional power sources

An interesting concept discussed was aligning AI workloads with periods when renewable energy is available.

---

# 14. AI Security

Three concepts were discussed:

## A. Back-Translation Defense

Used particularly against **jailbreaks**.

Basic idea:

**Potential harmful output → infer the original prompt → run the inferred prompt through safety filters**

This can help detect prompts that bypass normal moderation through clever wording.

---

## B. PIRA / PIRATE-type Risk Detection

The discussion described an open-source Python-based approach/library for identifying different categories of AI risks.

Potentially:

* Identify risk categories
* Train/extend risk classifiers
* Add additional languages
* Expand risk categories

---

## C. Security Fine-Tuning

AI models that generate code can potentially produce:

* Malware
* Vulnerable code
* Code that improperly sends data externally

Fine-tuning models on **security-curated datasets and security practices** can help reduce these risks.

---

# 15. AI Coding Assistants & Company Code

Companies often restrict developers from using public AI coding tools because of concerns about:

* Source-code leakage
* Intellectual property
* Confidential information
* Third-party model training
* Security

### Possible solution

Deploy an AI coding assistant:

**Inside the company's infrastructure**

and potentially:

**Fine-tune it using the company's own repositories and coding practices.**

Benefits:

* Better alignment with company coding standards
* Reduced data leakage concerns
* Better understanding of internal repositories
* More relevant code generation

---

# 16. Where AI Coding Assistants Can Be Particularly Useful

A particularly interesting use case mentioned was **migration work**.

Examples:

* Programming-language migration
* Security-package migration
* Infrastructure migration
* Large-scale code transformation

AI can perform much of the repetitive transformation while humans provide **manual oversight**.

---

# 17. Skills Required for an AI/R&D Career

The discussion gave several recommendations for students.

### Most important: Fundamentals

Don't assume today's AI tools will remain the same.

Technology changes rapidly.

Therefore, fundamentals remain valuable.

Examples:

* Computer science fundamentals
* Mathematics
* Programming
* ML fundamentals
* Research methodology

### Other important skills

* Interdisciplinary understanding
* Curiosity
* Open-mindedness
* Ability to ask questions
* Continuous learning
* Willingness to challenge existing practices
* Ability to conduct research

### Important principle

> **Don't learn only today's tools. Learn the concepts that allow you to adapt to tomorrow's tools.**

---

# 18. Research Is Not Limited to an "R&D Job"

One speaker emphasized that research can happen in almost any role:

* Consulting
* Development
* Testing
* Red teaming
* Product work
* Engineering
* R&D

Client problems themselves can become research questions.

### AI changes rapidly

Therefore:

**Continuous learning is essential.**

You cannot become "fully caught up" with AI once and stop learning.

---

# 19. Why Do We Need a Global AI Framework?

Three major reasons were discussed:

### 1. Benefits should reach everyone

AI should benefit:

* Global North
* Global South
* East
* West

### 2. Avoid concentration of resources

AI resources shouldn't become concentrated in:

* One country
* One company
* One region
* One group of stakeholders

### 3. Global social and cultural values

AI systems should consider broader:

* Social values
* Cultural values
* Human values
* Equity
* Sustainability

---

# 20. Why Is AI Regulation Difficult?

AI is a **dual-use technology**.

The same technology can potentially be used for beneficial or harmful purposes.

A comparison from the discussion was essentially:

> A knife can be used to cut a cake or harm someone.

Therefore, regulation has a difficult balance:

**Prevent harm**

while simultaneously

**not preventing beneficial innovation.**

Other challenges:

* Technology evolves rapidly.
* Regulators may lack technical expertise.
* AI crosses national boundaries.
* Different countries have different priorities.
* Regulation takes time.

---

# 21. India's AI Regulation

The discussion characterized India's approach as relatively cautious / **"wait and watch"** at that point.

The anticipated direction mentioned was a combination of:

* Self-regulation
* Co-regulation
* Some stricter regulation where necessary

An important point:

> India may need approaches suited to its own diverse social and economic conditions rather than simply copying another country's regulatory framework.

---

# 22. AI Regulation Needs Multiple Perspectives

AI governance shouldn't be purely technical.

It should consider:

### Technical

* Models
* Security
* Infrastructure
* Performance

### Legal

* Privacy
* Copyright
* Liability
* Regulation

### Process

* How AI is developed and deployed

### Governance

* Accountability
* Oversight
* Responsible AI

---

# 23. AI as a Tool, Not Everything

This was one of the strongest final messages.

Think of:

> **AI as one tool in your toolbox.**

Not:

> **AI as the solution to every problem.**

The recommended mindset:

**Problem → Understand → Choose appropriate technology → Deploy → Measure outcome**

rather than:

**AI → Find somewhere to use it**

---

# 24. Responsible AI — Everyone Has a Role

Responsible AI isn't only the responsibility of:

* AI researchers
* Governments
* Companies

It involves:

* Developers
* Users
* Researchers
* Policymakers
* Students
* Organizations
* Society

Students were encouraged to participate in conversations around:

* AI policy
* AI regulation
* Responsible AI
* AI deployment

---

# 25. AI for Social Change

The discussion was optimistic about AI's potential in:

* Governance
* Education
* Environment
* Public services
* Data-driven decision making

But the technology needs to be used with:

### Prudence

Careful judgment about how and where AI should be applied.

### Temperance

Avoiding excessive or uncontrolled use.

The philosophical idea of **prudence** was highlighted as particularly relevant.

---

# 26. AI for Rural & Underserved Communities

A concern was raised:

> If rural populations don't have sufficient access to smartphones, computers, infrastructure, or digital literacy, could AI increase inequality rather than reduce it?

The proposed approach was:

### "Bottom of the pyramid"

Start by solving problems for the least-resourced users.

For example:

Instead of designing AI only for highly resourced schools:

**Start with government-school teachers and resource-constrained environments.**

If the solution works under those difficult conditions, it can potentially work in better-resourced environments too.

---

# 27. Most Important Takeaways

If you want to remember the entire discussion in **10 points**, remember these:

1. **AI competition will continue**, but scaling may eventually face limitations.
2. **AI is becoming a business/revenue generator**, not only a technology experiment.
3. **Democratization matters** — open-source, small and large models can coexist.
4. **Don't use GenAI for everything** — choose technology based on the actual problem.
5. **AI creativity is different from human creativity** because intention, experience, intuition and instinct matter.
6. **Hallucination isn't automatically creativity**; acceptable hallucination depends on the use case.
7. **Enterprise AI should protect customer data**, potentially through private infrastructure and customized models.
8. **AI sustainability matters** — smaller models, efficient hardware, edge AI and model orchestration can reduce compute.
9. **Responsible AI requires technical + legal + governance + social perspectives.**
10. **AI should be treated as a tool, not as the answer to every problem.**

### One-line philosophy of the whole session

> **Understand the problem first, choose the right AI—or non-AI—technology, deploy it responsibly, and consider its human, social, economic and environmental consequences.**


