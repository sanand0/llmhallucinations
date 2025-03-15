---
marp: true
theme: gaia
class: gaia
paginate: true
---

<!-- _backgroundColor: purple -->

# Visualizing LLM Hallucinations

### [Anand S](https://s-anand.net/)

###### LLM Psychologist @ Straive

![h:180px](https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://sanand0.github.io/llmhallucinations/)

Slides: [sanand0.github.io/llmhallucinations](https://sanand0.github.io/llmhallucinations)

---

![bg right cover](img/robo-psychologist.webp)

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

## LLMs have biases

![bg right cover](https://media.licdn.com/dms/image/v2/D5622AQE2Cfp6bE-Klg/feedshare-shrink_1280/feedshare-shrink_1280/0/1713171166756?e=1744848000&v=beta&t=EJWU59HgJLNTF5ZJEliwqRPqpaIkoHKKOzOGoltJTPo)

Try asking an LLM:

> Pick a random number from 0 - 100.
>
> Write ONLY the number NOTHING ELSE.

Try different `temperature`s.

[llmrandom.straive.app](https://llmrandom.straive.app) 🔗 [![invert](https://github.githubassets.com/favicons/favicon.svg)](https://github.com/sanand0/llmrandom)

---

<!-- _backgroundColor: #fff -->
<!-- _color: #212529 -->

## LLMs _are_ improving. Hallucinations _are_ reducing

![bg fit left:60%](https://media.licdn.com/dms/image/v2/D5622AQEarWKYoF-TsA/feedshare-shrink_1280/feedshare-shrink_1280/0/1723287574173?e=1744848000&v=beta&t=csvNmmQS6T49Y-GXmlk56TiTS6IyDa3ZVctyexqrxDI)

But errors add up in Agents, Computer use.

[LLM Pricing](https://llmpricing.straive.app) 🔗 [![](https://github.githubassets.com/favicons/favicon.svg)](https://github.com/gramener/llmpricing)

---

## Hallucinations can help

<!-- _backgroundColor: #000300 -->

![bg fit right:40%](https://upload.wikimedia.org/wikipedia/commons/c/cc/Digital_rain_animation_medium_letters_shine.gif)

- Penicillin
- Post-it notes
- Pacemakers
- Microwave ovens
- Surrealism / modern art
- Psychedelic Rock
- The Matrix

---

# I check for hallunications in 3 ways

1. **Logprobs**
   LLMs tell you the probability of each word they generate.
   ![h:20px](https://placehold.co/1x1/transparent/transparent)
2. **Embeddings**
   LLMs tell you the numerical closeness of 2 pieces of text.
   ![h:20px](https://placehold.co/1x1/transparent/transparent)
3. **LLM as a judge**
   LLMs don't _often_ make mistakes. Let them cross-check each other.

---

# Logprobs

<!-- _backgroundColor: #fff -->
<!-- _color: #212529 -->

![bg right contain](https://llmviz.straive.app/dog-laying-tracks-like-llm-word-by-word.avif)

[OpenAI API](https://platform.openai.com/docs/api-reference/chat/create#chat-create-logprobs) gives "logprobs".

```json
{
  "model": "gpt-4o-mini",
  "messages": [...],
  "logprobs": true,
  "top_logprobs": 5
}
```

```json
{ "token": " and", "logprob": -0.018 },
{ "token": " but", "logprob": -4.232 },
```

---

<!-- _backgroundColor: #fff -->
<!-- _color: #212529 -->

# Let's visualize these logprobs

> Concisely list 5 inventions created by human error or hallucinations

![](img/logprobs-visualization.webp)

[llmviz.straive.app](https://llmviz.straive.app) 🔗 [Prompt](https://llmfoundry.straive.com/playground#?template=Hallucinations) 🔗 [![](https://github.githubassets.com/favicons/favicon.svg)](https://github.com/sanand0/llmviz)

---

<!-- _backgroundColor: #fff -->
<!-- _color: #212529 -->

# Embeddings quantify similarity

[![h:500px](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgzOCWLMCxaOTTpZKlTr-o3t4l2Uq_IekgKg8P-1nM1OdwonDOiNs0ZCXaMbv12MMTMrstCb2NuKVwS2Oalw7R615Agjr2dkU6-P31BTQxZCHrBAQWJynwROgxFTuHCpwQzTPQauoDd5JQ/s1600/embedding-mnist.gif)](https://projector.tensorflow.org/)

---

<!-- _backgroundColor: #fff -->
<!-- _color: #212529 -->

# Embeddings highlight hallucinations

![bg right:30% contain](img/embedding-network.gif)

Examples:

[What LLMs do marketers use?](https://gramener.com/docsearch/insiderintelligence/)
[What's the Thailand strategy?](https://gramener.com/docsearch/insiderintelligence/)
[What TikTok's Thailand strategy?](https://gramener.com/docsearch/insiderintelligence/)

---

![bg right](img/contract-analysis.gif)

# LLM as a judge

LLMs can evaluate humans and other LLMs.

This works better than embeddings.

For example, which clauses are missing in a contract?

[contractanalysis.straive.app](https://contractanalysis.straive.app) 🔗 [![invert](https://github.githubassets.com/favicons/favicon.svg)](https://github.com/gramener/contractanalysis)

---

# Summary

<!-- _backgroundColor: purple -->

To check for hallucinations, explore these 3 techniques in order:

|     | Technique            | Cost | Quality |
| :-- | :------------------- | :--- | :------ |
| 1   | Logprobs             | Free | Low     |
| 2   | Embedding similarity | Low  | Medium  |
| 3   | LLM as a judge       | High | High    |

Slides: [sanand0.github.io/llmhallucinations](https://sanand0.github.io/llmhallucinations)

![bg right:30% fit](https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://sanand0.github.io/llmhallucinations/)
