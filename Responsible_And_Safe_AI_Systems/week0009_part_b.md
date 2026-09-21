# RSAI Live session with students

* structured summary of the **AI Safety / Responsible AI course discussion** in the transcript.

## 1. What the course will cover

The instructor explains that the course will progressively cover:

* **AI capabilities**
* **AI risks**
* **Bias**
* **Differential privacy / privacy**
* **AI safety**
* **Unlearning**
* **Domain-specific AI safety**, such as:

  * AI + law
  * AI + education
  * other application domains
* **Recent/trending AI safety topics**
* Expert discussions and Q&A sessions with researchers and practitioners.

The later part of the course will include recorded conversations/panels with prominent researchers, rather than being purely lecture-based. 

---

# 2. Prerequisites and learning expectations

The instructor makes an important point about prerequisites.

The course could have formally required knowledge of things like:

* Python
* Machine Learning
* Transformers
* Encoder-decoder architectures

But imposing too many prerequisites would exclude students from different backgrounds.

Therefore, the expectation is that students should **learn beyond the course material themselves**.

The course isn't intended to mean:

> "Attend these three hours and you will know everything."

Instead, students are expected to develop additional knowledge independently.

---

# 3. AI safety vs AI errors — an important discussion

One student asks:

> Why is bias considered an AI safety problem when ordinary misclassification or incorrect predictions can also cause harm?

For example:

* A biased AI can cause harm.
* A stock-market AI making a bad prediction could potentially cause enormous financial damage.

So what makes something specifically an **AI safety problem**?

The instructor's response is that the boundaries aren't completely standardized yet.

Problems such as:

* bias
* misinformation/fake news
* misclassification
* unreliable predictions
* inability to explain decisions

can potentially fall under **responsible AI / AI safety**, depending on how the problem is defined and interpreted.

The field is still evolving.

---

# 4. AI safety terminology isn't completely standardized

This was one of the most interesting discussions.

The student asks whether there should be standardized categories such as:

* Alignment problems
* Responsible AI problems
* AI safety problems
* Training problems
* Evaluation problems

The instructor agrees that this is an area where standardization is developing.

Organizations such as **NIST** are working on frameworks and terminology.

The key point:

> AI safety is still a relatively young field, so different researchers may use different terminology for related problems.

Over time, these concepts may converge into more standardized definitions.

---

# 5. Research opportunities around AI safety

The instructor points students toward emerging research areas.

One mentioned example is **deception in LLMs**.

The instructor recommends looking at an external report that categorizes different AI alignment/safety problems.

This report can help students understand the broader landscape of:

* alignment
* safety
* deception
* other AI risks.

---

# 6. Student-proposed red-team project

One student proposes a practical project:

Take an existing pretrained model and:

1. Choose a specific use case.
2. Red-team the model.
3. Find weaknesses.
4. Test for bias.
5. Perform fairness analysis.
6. Document the results.
7. Produce a report.

The instructor strongly supports the idea.

However, he says the project should be **student-driven**, because it isn't required for grades.

Students interested in participating should organize themselves and reach a critical mass.

This is a very practical idea because it converts AI safety from **theory → actual testing**.

---

# 7. A very useful point for industry professionals

One student says they come from industry rather than academia and asks:

> Is watching the lectures enough, or should I be reading research papers and doing additional material?

The instructor's response is essentially:

### Be specific about what you want to learn.

If someone asks:

> "I want to learn machine learning."

That's too broad.

But if they say:

> "I'm implementing Llama 3 and I'm having difficulty with this specific experiment."

or:

> "I'm using Hugging Face for this particular job and don't understand this part."

then the instructor can provide much more targeted help.

### The principle:

**Specific problem → specific learning → specific guidance.**

This is especially relevant for people coming from industry.

---

# 8. The course is intentionally not purely exam-oriented

The instructor explicitly pushes back against studying only for marks.

He acknowledges that students naturally want good scores, but argues that:

> Knowing something for an exam is different from actually understanding it.

The purpose of the course is to understand the subject, not simply chase marks for individual questions.

This is particularly important because AI safety is a rapidly changing field.

---

# 9. Week structure

The instructor explains that:

### Week 1–2

More focused on:

* AI capabilities
* AI risks
* foundational concepts

Week 2 is intentionally quite heavy.

### Week 3–4

Focus more heavily on topics such as:

* Bias
* Responsible AI

### Later weeks

More technical/theoretical material, including:

* Differential privacy
* Privacy
* AI safety
* Mathematical/theoretical concepts

Some later weeks are described as **theory-heavy and math-heavy**.

---

# 10. AI safety is broader than just "AI alignment"

The transcript repeatedly highlights that AI safety is a broad umbrella.

Potential areas include:

**Bias**

↓

**Privacy**

↓

**Fairness**

↓

**Reliability**

↓

**Misinformation**

↓

**Deception**

↓

**Alignment**

↓

**Human oversight**

↓

**Domain-specific risks**

The boundaries between these areas are not always universally agreed upon.

---

# 11. NIST and regulatory work

An interesting part of the discussion involves students who have already worked with NIST material.

One student mentions participating in work around:

* NIST
* Generative AI
* AI safety
* regulatory frameworks
* EU AI Act Article 14 / human oversight

The instructor encourages them to connect offline and potentially collaborate on reviewing/commenting on the relevant reports.

This shows that the course isn't just theoretical—the instructor is encouraging students to engage with **real-world standards and regulatory work**.

---

# 12. Practical research mindset

The instructor encourages students to go beyond:

> Lecture → Assignment → Exam

Instead:

> **Lecture → Question → Research → Experiment → Discussion**

For students particularly interested in AI safety, he encourages:

* research projects
* master's thesis work
* collaborative projects
* reviewing reports
* practical experiments
* red teaming

---

# 13. Overall message of the transcript

The biggest message is:

### AI safety is a rapidly evolving multidisciplinary field.

You don't just need to understand AI models.

You also need to understand:

* **What the model can do**
* **How it can fail**
* **Why it fails**
* **Who can be harmed**
* **How to measure the harm**
* **How to test the model**
* **How to mitigate the risk**
* **How humans should oversee it**
* **How regulation should apply**

And importantly, the field itself is still developing its terminology and standards.

---

## The part I think is particularly relevant to your career

Given that you're a **Testing Engineer**, one idea from this transcript stands out:

### Red teaming an AI system

The student's proposed project is almost directly connected to **AI Testing**:

**Take model → define use case → attack/test it → identify failures → test bias/fairness → document findings.**

That is much closer to **AI Quality Engineering / AI Safety Testing** than simply learning prompt engineering.

You could eventually think of your testing mindset as:

> **Traditional QA:** Does the software behave according to requirements?

> **AI Testing:** How does the AI behave across normal, edge, adversarial, biased, ambiguous, and unexpected situations?

> **AI Safety Testing:** What happens when the AI's behavior creates unacceptable risk?

That progression connects very naturally with the course topics discussed in this transcript.
