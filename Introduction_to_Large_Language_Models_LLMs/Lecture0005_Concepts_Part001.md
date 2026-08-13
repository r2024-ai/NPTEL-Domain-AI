# How neural network work?

The diagram is trying to make a connection between a **biological neuron** and the **mathematical model of an artificial neuron**, which is the basic building block of a neural network.

The nice thing is that the diagram is actually showing the idea from **biology → abstraction → mathematics**.

## 1. First, understand the biological neuron

The important parts are:

### Dendrites

The tree-like structures on the left are **dendrites**.

Their job is essentially:

> **Receive signals from other neurons.**

Your diagram even says:

> "dendrite — receives signals from other neuron"

So imagine many neurons sending information toward this neuron.

---

### Soma / cell body

The central part is the **soma**, or cell body.

Your diagram says:

> "Soma — processing the information"

That's the important conceptual jump.

The soma receives signals coming through the dendrites and participates in deciding whether the neuron should generate an output signal.

For a simplified neural-network analogy:

**Soma ≈ computational unit**

---

### Axon

The long structure leaving the soma is the **axon**.

It carries the neuron's output signal toward other neurons.

Your diagram says something like:

> "axon — transmits the output of a neuron to another neuron"

So:

**Dendrites → receive**

**Soma → process**

**Axon → transmit**

---

### Synapse

At the end, neurons communicate through connections called **synapses**.

Your diagram labels:

> "Synapse — point of connection to other neuron"

This is particularly important for understanding neural networks because the **strength of these connections** is analogous to the **weights** in an artificial neural network.

---

# 2. Now comes the clever part: turning the neuron into mathematics

Look at the bottom-right of your diagram.

You have:

$$
x_1,;x_2,;\ldots,;x_n
$$

going into a mathematical unit, and an output:

$$
y
$$

coming out.

The diagram labels the function as something like:

$$
f(\ )
$$

This is the abstraction of the biological neuron.

Instead of worrying about all the biological details, we say:

> "Let's treat the neuron as a mathematical function."

So we can write:

$$
y=f(x_1,x_2,\ldots,x_n)
$$

This is the fundamental idea.

---

# 3. Where do the $(x_1,x_2,\ldots,x_n)$ come from?

Think of them as signals coming from other neurons.

For example:

```text
Neuron 1 ──→ x₁ ──┐
Neuron 2 ──→ x₂ ──┤
Neuron 3 ──→ x₃ ──┤──→ [ neuron ] ──→ y
       ...         │
Neuron n ──→ xₙ ──┘
```

The artificial neuron receives multiple inputs.

These inputs might represent:

* information from previous neurons
* features of a data point
* outputs of another layer

---

# 4. But all inputs are not equally important

This is where **weights** enter.

Suppose we have three inputs:

$$
x_1,;x_2,;x_3
$$

We associate a weight with each:

$$
w_1,;w_2,;w_3
$$

Then instead of simply adding the inputs, we calculate:

$$
w_1x_1+w_2x_2+w_3x_3
$$

More generally:

$$
\sum_{i=1}^{n}w_ix_i
$$

This is the core computation performed by a basic artificial neuron.

### Intuition

Think of the weights as **importance factors**.

For example:

$$
w_1=0.9
$$

means input $(x_1)$ has a relatively strong influence.

Whereas:

$$
w_2=0.1
$$

means $(x_2)$ has a relatively weak influence.

A negative weight can mean that an input pushes the output in the opposite direction.

---

# 5. Usually there is also a bias

A basic artificial neuron is generally written:

$$
z=w_1x_1+w_2x_2+\cdots+w_nx_n+b
$$

or more compactly:

$$
z=\mathbf{w}^T\mathbf{x}+b
$$

Then we apply an **activation function**:

$$
y=f(z)
$$

So the complete picture becomes:

$$
\boxed{
x_1,x_2,\ldots,x_n
\rightarrow
\text{weighted sum}
\rightarrow
\text{activation function}
\rightarrow
y
}
$$

This is much closer to what your bottom-right drawing is trying to represent.

---

# 6. Why do we need the activation function?

This is an extremely important concept.

Suppose we only did:

$$
y=w_1x_1+w_2x_2+b
$$

Then the neuron would just perform a **linear transformation**.

Activation functions introduce **non-linearity**.

For example, one common activation function is ReLU:

$$
f(z)=\max(0,z)
$$

So:

$$
z=-3 \Rightarrow f(z)=0
$$

while:

[
z=5 \Rightarrow f(z)=5
]

This allows neural networks to learn much more complicated relationships.

---

# 7. Biological neuron → artificial neuron mapping

This is probably the most useful thing to keep in your notes.

| Biological neuron               | Artificial neural network          |
| ------------------------------- | ---------------------------------- |
| Dendrites                       | Input signals $(x_1,x_2,\ldots,x_n)$ |
| Synaptic connections            | Weights $(w_1,w_2,\ldots,w_n)$       |
| Soma/cell body                  | Computation                        |
| Neuron's integration of signals | Weighted sum                       |
| Neuron activation               | Activation function                |
| Axon                            | Output $(y)$                         |
| Network of neurons              | Neural network                     |

But **be careful**:

> This is an analogy, not a literal biological simulation.

Artificial neurons are mathematical abstractions inspired by biological neurons. They don't reproduce everything that a real neuron does.

---

# 8. How does one neuron become a neural network?

This is the next conceptual step.

One artificial neuron:

$$
x_1,x_2,\ldots,x_n
\rightarrow
\boxed{\text{neuron}}
\rightarrow y
$$

Many neurons together form a **layer**.

For example:

```text
Input layer          Hidden layer          Output

x₁ ───────────────→  ○ ────────┐
x₂ ───────────────→  ○ ────────┤
x₃ ───────────────→  ○ ────────┤──→ ○ → y
x₄ ───────────────→  ○ ────────┤
                   ○ ──────────┘
```

And then multiple layers:

```text
Input             Hidden             Hidden             Output

x₁ ───┐          ○ ───┐             ○ ───┐
x₂ ───┼────────→ ○ ───┼──────────→  ○ ───┼──→ y
x₃ ───┤          ○ ───┘             ○ ───┘
x₄ ───┘
```

That's the basic idea behind a **feed-forward neural network**.

---

# 9. The really important conceptual shift

Don't memorize:

> "A neural network is many neurons connected together."

Instead understand this:

### A neural network is a mathematical function built by composing many simple functions.

For example:

$$
\mathbf{x}
\rightarrow
f_1
\rightarrow
f_2
\rightarrow
f_3
\rightarrow
y
$$

You can think of it as:

$$
y=f_3(f_2(f_1(x)))
$$

Each layer transforms the information received from the previous layer.

That's why the diagram is moving from a biological neuron to:

$$
f(x)
$$

It's essentially saying:

> **Let's abstract the neuron into a function.**

And then:

> **Let's connect many such functions together.**

That becomes a neural network.

---

# Self-notes — Neural Network from a Neuron

You can keep the following as your study notes:

## Neural Network — Basic Idea

### 1. Biological inspiration

A biological neuron has three important conceptual components:

* **Dendrites** → receive signals from other neurons
* **Soma (cell body)** → integrates/processes incoming signals
* **Axon** → transmits the output signal to other neurons
* **Synapse** → connection through which neurons communicate

### 2. Artificial neuron

An artificial neuron abstracts this idea mathematically.

It receives inputs:

$$
x_1,x_2,\ldots,x_n
$$

Each input has an associated weight:

$$
w_1,w_2,\ldots,w_n
$$

The neuron first computes:

$$
z=\sum_{i=1}^{n}w_ix_i+b
$$

where:

* (x_i) = input
* (w_i) = weight/importance of input
* (b) = bias
* (z) = weighted sum before activation

Then an activation function is applied:

$$
y=f(z)
$$

Therefore:

$$
\boxed{y=f\left(\sum_{i=1}^{n}w_ix_i+b\right)}
$$

### 3. Interpretation

The artificial neuron can be thought of as:

$$
\boxed{\text{Inputs} \rightarrow \text{Weighted combination} \rightarrow \text{Activation} \rightarrow \text{Output}}
$$

### 4. Connection to biology

| Biology           | Artificial NN       |
| ----------------- | ------------------- |
| Dendrites         | Inputs              |
| Synaptic strength | Weights             |
| Soma              | Computation         |
| Neuron activation | Activation function |
| Axon              | Output              |

This mapping is **conceptual/analogical**, not an exact biological simulation.

### 5. From neuron to neural network

One neuron:

$$
y=f(\mathbf{w}^T\mathbf{x}+b)
$$

Multiple neurons → **layer**

Multiple layers → **neural network**

A neural network can therefore be viewed as a composition of functions:

$$
\boxed{
\mathbf{x}
\rightarrow
f_1
\rightarrow
f_2
\rightarrow
\cdots
\rightarrow
f_L
\rightarrow
y
}
$$

### 6. Most important idea to remember

> **An artificial neuron is a mathematical function that combines multiple inputs using learnable weights and bias, then applies an activation function.**

> **A neural network is a collection of these computational units arranged in layers, where the parameters (weights and biases) are learned from data.**

---

## One thing I'd suggest you understand next

Don't jump immediately into **CNN, RNN, Transformer, backpropagation, etc.**

Build the foundation in this order:

$$
\boxed{
\text{Neuron}
\rightarrow
\text{Weights}
\rightarrow
\text{Bias}
\rightarrow
\text{Activation}
\rightarrow
\text{Layer}
\rightarrow
\text{Neural Network}
\rightarrow
\text{Loss}
\rightarrow
\text{Gradient}
\rightarrow
\text{Backpropagation}
\rightarrow
\text{Training}
}
$$

Once these pieces click, **"how does a neural network learn?"** becomes a much less mysterious question.
