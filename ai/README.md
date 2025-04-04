# TaxDown AI Scientist Challenge

## About the position

You will be at the forefront of applying cutting-edge AI to revolutionize how we deliver TaxDown's high-quality, personalized tax advice. Our team is building intelligent agents that work alongside our expert tax advisors, helping them scale their work while maintaining our high standards of quality.

Data is at the core of our business, and we're uniquely positioned to rapidly develop AI solutions that deliver real, measurable impact. While we've had initial success with sophisticated prompting techniques, we need someone who can stay ahead of the curve in the fast-moving world of AI.

You will explore, evaluate, and implement the latest AI trends and techniques, working closely with our engineers and tax experts to bring these powerful solutions to life. This is your chance to make your mark in a newly formed team, learn incredibly fast in a dynamic environment, and grow your expertise alongside passionate colleagues.

We value learning, experimentation, and pushing boundaries. We want you to bring your unique perspective, help us learn, and become an even more impactful AI expert with us (the real "Win - Win" 🚀).

👂 *We value robust, interpretable, and well-documented AI solutions. Show us how you think about safety, edge cases, and potential biases in your implementation.*

## Take me to the challenge! 🤟

One of the exciting areas we're working on involves using AI agents, powered by LLMs, to handle user interactions and automate certain tasks. However, automating actions, especially sensitive ones related to taxes is tricky stuff! A mistake could impact users or even cause issues with the Tax Agency.

That's why building robust **guardrails** is crucial. These guardrails need to ensure our agents only perform sensitive actions when they're *absolutely* sure and all conditions are met.

In this challenge (don't worry, we don't want you to do work for free, we'll keep it focused!), you'll design and implement a proof-of-concept for one AI guardrail specifically for the IBAN update process of our clients. This will give us great insight into how you approach these kinds of AI/NLP problems.

### The Goal 🎯

This guardrail needs to:

*   Accurately figure out if a user *really* wants to request an IBAN change and ensure the agent picks the right tool for the job.
*   Make *absolutely sure* the IBAN change tool only runs if **all** these conditions are met:
    *   The agent explicitly asked the client for confirmation to change the IBAN.
    *   The client provided the last 4 digits of their *current* IBAN (as requested by the agent), AND another check confirmed these digits are correct.
*   Verify that when the agent calls the IBAN change tool, it uses the right arguments, all correctly set up.

### What You Get (The Data) 🎁

We'll provide a synthetic **dataset** in `JSON` format. It's a list of simulated conversations between users (`human`), our AI agent (`ai`), and system tools (`tool`).

Each conversation is a list of messages structured like this:

*   `type`: Who's talking? (`human`, `ai`, `tool`).
*   `content`: What they said (or the tool's output if `type` is `tool`).
*   `tool_call`: If the `ai` decided to use a tool, you'll see this dictionary:
    *   `name`: The tool's name.
    *   `args`: The arguments passed to the tool.

Crucially, each conversation has a label: `fires_guardrail` (true/false), telling you if our ideal guardrail *should* have stepped in for that conversation.

Finally, here's the signature of the IBAN change tool our agent uses:

```json
{
  "tool_name": "change_iban",
  "tool_description": "Updates the user's bank account number (IBAN) in the system after verifying the last four digits of the currently saved user's IBAN and confirming the request.",
  "tool_arguments": {
    "new_iban": {
      "type": "string",
      "required": "true"
    }
  }
}
```

### Your Tasks - Step by Step 🌟

1.  **Dig into the Data & Prep:**
    *   Explore the `dataset`. What tools does the agent use? What do conversations look like?
    *   Do any necessary preprocessing to make it easier to work with for building and testing your guardrail.
    *   Quickly assess: Is this dataset good enough for the job? What are its strengths/weaknesses?

2.  **Design Your Guardrail:**
    *   What NLP or AI techniques make the most sense here? Explain your reasoning.
    *   Compare potential techniques. Think about:
        *   Cost (compute & money)
        *   Speed (latency)
        *   How well it works (quality)
        *   Can it scale?
        *   Is it easy to maintain?
        *   What data does it need for training?
        *   Can we understand *why* it makes a decision (interpretability)?
    *   Define exactly what your guardrail will *do* when it triggers (e.g., stop the agent, suggest a correction, etc.). Justify your choice!

3.  **Build It! (Proof of Concept):**
    *   Implement the approach you think is most promising.
    *   **Focus on the AI/NLP part.** We're more interested in your technical approach to the AI problem than perfect code architecture or following every single software engineering best practice (though clean, understandable code is always appreciated!).
    *   A `Jupyter notebook` is perfectly fine for this. Use libraries/frameworks you're comfortable with. Show your work and explain your steps!

4.  **Show Us It Works! (Evaluation):**
    *   This is super important! How will you *prove* your guardrail works reliably? Design an evaluation plan.
    *   Choose the right metrics and explain why they're relevant here.
    *   How would your evaluation approach give us confidence it would work in production?
    *   Implement the evaluation and give us a critical analysis of your results. What worked well? What didn't?

5.  **Thinking Ahead (Scalability & Improvements):**
    *   How could your solution handle way more conversations in real-time?
    *   Any ideas to make the `dataset` even better for assessing guardrails like this? How would you implement those improvements?

👂 *We value robust, interpretable, and well-documented AI solutions. Show us how you think about safety, edge cases, and potential biases in your implementation.*

### Using Tools like ChatGPT or Claude? 🤖

No problem! Many of us use them. If you do, just be transparent:

*   Share links to your conversations.
*   Document the prompts you used.
*   Show us the different iterations you went through.

### Time Estimate & Tips ⏰

This challenge is designed to take roughly **3-6 hours**. We know the scope is ambitious! Don't stress if you can't implement *everything* perfectly.

If time gets tight (say, after 4 hours):

*   Focus on getting a **basic, functional version** of the guardrail working.
*   For parts you didn't implement, **explain conceptually** how you *would* have done them.
*   Clearly document what's implemented and what's still in the design/conceptual phase.

👂 *Psst, remember to include clear instructions on how to set up and run your code!*

### How We'll Look At It 👀

What we value most is your **technical thinking** and how you reason about the problem. A well-thought-out approach, even if not 100% implemented, is better than a rushed, superficial solution.

We'll be looking at:

*   How deeply you understood the problem.
*   Your creativity, effectiveness, and how well you justify your solution.
*   The technical quality of your AI/NLP approach.
*   The quality and suitability of your evaluation plan and results.

## How can I share my solution? 🔥

You've probably been using Git, right? 😉 How about creating a private GitHub repo and inviting us: [Joaquin Fernández](https://github.com/JoaquinFernandez) and [Alvaro Correa](https://github.com/corrius).

Your repo should contain:

1.  A `README.md` explaining your approach (data analysis, design, justification, run instructions).
2.  Your code (e.g., `Jupyter Notebook`) with the guardrail implementation.
3.  The results of your evaluation.
4.  Links/info about any AI assistant usage (if applicable).

This way, we can review your awesome work and have it ready for the next step: a chat with the team! 👻

Good luck with the challenge! Enjoy it and do your best!