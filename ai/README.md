# TaxDown AI Scientist challenge

## Context

At TaxDown, we use advanced language models (LLMs) to understand and accurately respond to our users' queries. One of the main approaches we are exploring is agents, which allow us to automate tasks related to certain intentions identified in these queries.

Automating these actions is particularly delicate, as an error in interpreting the user's intention or executing an automated action could lead to significant consequences, such as customer loss or compromising situations with the Tax Agency.

Therefore, when building these agents, we aim to automate only those actions in which we have high confidence. Additionally, as an extra security measure, we incorporate guardrails that question and validate decisions before executing any automated action.

## Objective

Design and implement a **guardrail** that can:

*   Accurately identify if the user's intention is to request an IBAN change, ensuring the agent uses the correct corresponding tool.
*   Ensure that the IBAN change tool is only executed when the following conditions are met:
    *   The agent has explicitly asked the client to confirm the IBAN change.
    *   The client has provided, at the agent's request, the last 4 digits of the IBAN currently configured in their profile, and an additional tool has validated that these digits match correctly.
*   Verify that the call to the IBAN change tool is always made with the appropriate and correctly configured arguments.

## Provided Data

A synthetic dataset simulating conversations with the agent is provided. These conversations contain user messages (`human`), agent messages (`ai`), and tool responses (`tool`).

The **dataset** is in JSON format and contains a list of labeled conversations.

A conversation is formed by a list of messages with the following structure:

*   `type`: type of message (`human`, `ai`, `tool`).
*   `content`: content of the message or the tool's response if the message is of type `tool`.
*   `tool_call`: dictionary with a function call. Only present in messages of type `ai`.
    *   `name`: name of the tool.
    *   `args`: dictionary with the arguments for the tool.

The label of the conversations (`fires_guardrail`) indicates whether the guardrail should be triggered or not.

### Tasks

#### Data Analysis and Preprocessing

Examine and analyze the **dataset** to understand the different tools the agent has. Perform the necessary transformations to facilitate the evaluation and testing of the guardrail. Analyze the quality and adequacy of the **dataset** in relation to the stated objectives.

#### System Design

*   Explain which NLP techniques or AI models you consider most suitable for developing a guardrail with these characteristics.
*   Compare the techniques using the following factors:
    *   Computational and financial cost
    *   Latency
    *   Quality of results
    *   Scalability
    *   Maintainability
    *   Training data requirements
    *   Model interpretability
*   Define and justify the behavior the guardrail will have (stopping the agent, correcting the tool call generation...).

### Implementation (Proof of Concept)

Develop the solution you consider most promising to address the problem. The main focus of the evaluation will be on the technical approach related to AI models, especially the application of NLP techniques to solve the stated problem.

Furthermore, the evaluation methodology you use to determine if the guardrail meets its objectives robustly and reliably will be particularly valued.

It should be noted that the objective is not to evaluate your software development skills or code best practices in depth. Therefore, we recommend focusing your time and effort on the technical design and execution of the AI solution, rather than on code architecture or formal aspects.

The code must be understandable and executable. A Jupyter notebook is sufficient, provided you document the different approaches you explore clearly and structurally. You can use any framework or library you are comfortable with. The most important thing is the result and that you work similarly to how you would in your day-to-day work.

### Evaluation

A crucial part of this technical test is the methodology you use to evaluate the effectiveness and reliability of the implemented guardrail. You should:

*   Design an evaluation framework that allows objective measurement of the guardrail's performance.
*   Select and justify the metrics you consider most relevant for this specific problem.
*   Explain how your evaluation approach would ensure the guardrail functions correctly in a real production environment.
*   Implement this evaluation and critically analyze the obtained results.

### Scalability and Improvements

*   Discuss how the implemented solution could be scaled to handle a large volume of messages in real time.
*   Propose possible improvements to the **dataset** so that the guardrail evaluations are as reliable as possible. Explain how you would carry them out.

### Use of tools like ChatGPT or Claude

We are aware that many people nowadays turn to tools like `ChatGPT` or `Claude` to develop their solutions. If you decide to use any of these tools during the development of your solution, it is essential that you:

*   Share the links to the conversations you have with them.
*   Document any prompt you use.
*   Provide all the iterations you perform during the development process.

### Deliverables

The deliverable must be a **GitHub repository** to which you should grant access to the user **@corrius**.

This repo must contain:

1.  A `README.md` file describing your approach, including:
    1.  Data analysis
    2.  Design of the approach (or approaches) to develop the guardrail.
    3.  Justification for the implemented solution.
    4.  Clear instructions to run the code.
2.  The source code (`Jupyter Notebook`):
    1.  With the guardrail implementation.
    2.  With the results of your solution's evaluation.
3.  Links to conversations and prompts used with tools like `ChatGPT` or `Claude` (if applicable).

### Completion Time

The test is designed for you to complete in about 3-6 hours. We know the scope is ambitious, so don't worry if you can't implement absolutely everything.

If you see that after 4 hours you won't be able to finish everything you'd like, we suggest you:

*   Focus on having a basic but functional version of the guardrail.
*   For the parts you don't have time to implement, explain how you would do them at a conceptual level.
*   Clearly document what you have implemented and what you have left in the design phase.

### Evaluation

What we value most is your technical approach and your way of reasoning about the problem, not so much the amount of code you produce. We prefer a well-thought-out solution, even if not fully implemented, over a complete but superficial implementation.

The evaluation will consider:

*   The depth of your analysis and understanding of the problem.
*   The creativity, effectiveness, and justification of the proposed solution.
*   The technical quality of the AI models and the problem resolution.
*   The quality and adequacy of the proposed evaluation framework.