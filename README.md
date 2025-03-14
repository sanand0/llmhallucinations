---
marp: true
theme: gaia
class: gaia
paginate: true
---

<!-- _backgroundColor: purple -->

# Visualizing LLM Hallucinations

### Anand S

###### LLM Psychologist @ Straive

![h:180px](https://placehold.co/1x1/transparent/transparent)

- Slides: [sanand0.github.io/llmhallucinations](https://sanand0.github.io/llmhallucinations)
- Website: [s-anand.net](https://s-anand.net/)

---

# I'm often asked: What's an LLM psychologist?

![h:200px](https://placehold.co/1x1/transparent/transparent)

I research how LLMs think.

---

# LLMs are more human than machine

Simon Willison:

> One way to think about it is that about 3 years ago, aliens landed on Earth. They handed over a USB stick and then disappeared.
>
> Since then, we’ve been poking the thing they gave us with a stick, trying to figure out what it does and how it works.

---

<!-- _backgroundColor: #212529 -->

## LLMs guess random numbers like humans

![bg right cover](https://media.licdn.com/dms/image/v2/D5622AQE2Cfp6bE-Klg/feedshare-shrink_1280/feedshare-shrink_1280/0/1713171166756?e=1744848000&v=beta&t=EJWU59HgJLNTF5ZJEliwqRPqpaIkoHKKOzOGoltJTPo)

```
Pick a random number from 0 - 100.
Write ONLY the number NOTHING ELSE.
```

![h:160px](https://placehold.co/1x1/transparent/transparent)

<https://llmrandom.straive.app>

---

<!-- _backgroundColor: #fff -->
<!-- _color: #212529 -->

## LLMs _are_ improving. Hallucinations _are_ reducing

![bg fit left:60%](https://media.licdn.com/dms/image/v2/D5622AQEarWKYoF-TsA/feedshare-shrink_1280/feedshare-shrink_1280/0/1723287574173?e=1744848000&v=beta&t=csvNmmQS6T49Y-GXmlk56TiTS6IyDa3ZVctyexqrxDI)

But errors add up in Agents, Computer use.

<https://llmpricing.straive.app>

---

# Hallucination isn't bad

We got:

- Penicillin
- Post-it notes
- Pacemakers
- Microwave ovens
- Surrealism / modern art
- Psychedelic Rock
- The Matrix

---

# I use 3 checks for hallunications

- Logprobs
- Embeddings
- LLM as a judge

---

# Logprobs

![bg right contain](https://llmviz.straive.app/dog-laying-tracks-like-llm-word-by-word.avif)

<https://llmviz.straive.app>

---

# Visualize embeddings

<https://gramener.com/docsearch>
Embedding distance can pinpoint hallucinations. Also citations. Embedding is better than log probs

---

# LLM as a judge

- Contract analysis. Contracts written by LLMs. Which ones made fewer mistakes? This is better than embeddings

---

# Summary

There are 3 techniques to check for hallunications. In increasing order of sophistication

- Logprobs
- Embeddings
- LLM as a judge

https://sanand0.github.io/llmhallucinations
