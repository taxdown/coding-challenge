# TaxDown AI Scientist / Engineer Challenge

## About the position

You will be helping us shape the future of how millions of people interact with AI-powered assistants.  
At **TaxDown**, we’ve been running production LLM systems for more than two years, serving **hundreds of thousands of users** and assisting our experts with **hundreds of thousands of AI-generated responses**.

Now we’re looking for someone who can help us push the boundaries even further — designing, evaluating, and iterating on intelligent agents that can reason, search, and improve over time.

We want you to bring your experience, creativity, and scientific rigor to our AI stack.  
And of course, we hope you’ll learn a lot from us too. The goal is mutual growth — the real “Win-Win” 🚀

---

## Take me to the challenge! 🤟

In this challenge (don’t worry, it’s short and fun — we don’t want free work 😉), you’ll design a **multi-agent system** for a **motorbike workshop assistant**.

The idea is to create an intelligent system that can **understand different types of questions** and **route them** to the right specialized agent.

You can use **any LLM**, **framework**, or **stack** you prefer (LangChain, DSPy, custom code…).  
You can also use AI tools (ChatGPT, Claude, Copilot, etc.) to help you — just tell us how.

---

## First step 🌟

Design a system that can receive questions from users and decide which agent should answer them.

Your system should be able to handle three types of questions:
1. **General questions** — about the workshop itself (schedule, prices, contact…).
2. **HR questions** — internal policies for employees (vacations, equipment, permissions…).
3. **Technical questions** — about motorbike maintenance and repair manuals (e.g., torque values, fluid capacities).

Each agent should respond based on different information sources:
- **General Agent:** uses workshop info.
- **HR Agent:** uses HR policies.
- **Manuals Agent:** retrieves information from the technical manuals in `/data/manuals/`.

You can use **any LLM**, **framework**, or **stack** you prefer (LangChain, DSPy, custom code…).  
You can also use AI tools (ChatGPT, Claude, Copilot, etc.) to help you — just tell us how.

That said, we’ll pay attention to **code quality and architecture**.  
We expect clear, extensible, and modular code — not a single messy script.  
Design decisions that show good practices like **SOLID**, clean interfaces, or proper separation of concerns will be valued positively.

💡 You decide how to design the routing and the agents — chain, graph, router LLM, or logic rules.

---

## Second step 🧠

Evaluate your system using the provided **`EVAL.md`** file.

This evaluation set includes different types of questions:
- Simple ones that can be answered from a single manual
- Others that require combining information from multiple sources
- System-level questions (e.g. carburetion vs. injection)
- And two questions with **no valid answer** — your agent should detect and handle those gracefully, rather than guessing
    
You should:
- Run your system on all questions in `EVAL.md`
- Show the reasoning traces (how routing decisions were made, what each agent did)
- Identify one case that didn’t work well, analyze why, and iterate on your prompt or logic to improve it

🧩 _The goal is to understand how you evaluate, debug, and improve your own system — not to get everything right on the first try._

---

## Third step 🧰

Document your work.

Include:
- How to run your system.
- How to reproduce the evaluation.
- A short note on what tools or AI assistants you used (ChatGPT, Claude, etc.) and in what way.
- Any reflections on how you’d take this to production.
    
📝 _We’re more interested in your reasoning and iteration process than in production polish._

---

## Rules for using AI as an assistant 🤖

You can use AI tools like ChatGPT, Claude, Copilot, Codex, etc. to help you during the challenge — just as you would at work.  
These rules only apply to the AI that helps you solve the challenge (not the AI agents you build).

1. **Transparency:** mention where and how you used AI.
2. **Responsibility:** you’re still accountable for the final code and decisions.
3. **Attribution:** cite any external or AI-generated content you include.
4. **Cost:** if you use paid APIs, include a brief note on estimated usage.
    
---

## What we’ll be looking for 👌

Some of the things we’d love to find in your solution (not necessarily all):
- Clear reasoning behind design choices
- Well-structured prompts and data flow
- Simple but functional retrieval system
- Traceable logic and introspection
- Evaluation and iteration methodology
- Pragmatic engineering mindset

---

## How can I share my solution? 🔥

Create a **private GitHub repo** with your solution and **add @corrius as a collaborator**.

Include:
- `RUN.md` — how to execute your system
- `TRACE.md` — sample traces of your agents’ reasoning
- `EVAL.md` — your mini evaluation and analysis
- `AI_USAGE.md` — how you used AI tools during the challenge

That’s it. We’ll review your work and schedule a short technical conversation to dive deeper together. 👻

Good luck with the challenge — and have fun with it! 🏍️
