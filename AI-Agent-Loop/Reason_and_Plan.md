# Reason and Plan & ReAct

## Quick Overview

| Name            | Definition                                                                                | Example                                     |
| --------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------- |
| Reason and Plan | The agent thinks about the goal and creates steps before acting.                          | Breaking “book a flight” into smaller tasks |
| ReAct           | A method where an AI alternates between reasoning, taking actions, and observing results. | Think → Search → Observe → Think → Act      |

## 1. Reason and Plan

**Definition:** Reason and Plan is the stage where an AI agent thinks about what it needs to do before taking action.

The agent starts with a **goal** and the information it already knows. It breaks the goal into smaller steps, checks the steps, and creates a logical order for completing them.

**Example:**

```text
Goal: Book a flight

1. Find available flights
2. Compare prices
3. Select the best flight
4. Enter passenger details
5. Complete the booking
```

**Instructions:**

* Start with a clear goal.
* Break the goal into smaller, manageable steps.
* Put the steps in a logical order.
* Consider possible problems and backup actions when necessary.

## 2. ReAct

**Definition:** ReAct (Reasoning + Acting) is an approach where an AI model **reasons and takes actions in an alternating process**.

Instead of creating a complete plan and acting without checking the results, the agent can reason, take an action, observe the result, and then reason again.

**Example:**

```text
Goal: Find the capital of a country

Thought → I need reliable information.
Action → Search a knowledge source.
Observation → The result says the capital is Paris.
Thought → The information answers the question.
Action → Give the final answer.
```

**Instructions:**

* **Reason:** Decide what to do next.
* **Act:** Use a tool or interact with an environment.
* **Observe:** Check the result of the action.
* Repeat the cycle when more information or actions are needed.
* ReAct can help ground answers in external information and handle unexpected results.

## 3. Reasoning vs. Acting

**Definition:** Reasoning helps the AI decide what to do, while acting allows it to interact with external tools or environments.

ReAct combines both instead of treating them as separate processes.

**Example:**

```text
Reasoning only:
"I think the answer is X."

Acting only:
"Search for information → Get result → Stop."

ReAct:
"Think → Search → Observe → Think → Answer"
```

**Instructions:**

* Reasoning helps create and update action plans.
* Actions provide new information from external sources.
* Observations allow the agent to adjust its next step.
* Combining reasoning and acting can reduce errors caused by relying only on internal knowledge.

## 4. ReAct Prompting

**Definition:** ReAct prompting teaches an AI model to follow a pattern of reasoning, actions, and observations using examples in the prompt.

The original ReAct work used **few-shot examples** containing reasoning traces, actions, and observations from the environment.

**Example:**

```text
Example:

Thought → I need to find the product.
Action → Search for the product.
Observation → Product found for $50.
Thought → I should compare its price.
Action → Search another store.
Observation → Same product costs $45.
Answer → The second store has the lower price.
```

**Instructions:**

* Provide examples showing how reasoning and actions work together.
* Allow the model to use observations to update its approach.
* ReAct can be applied to tasks such as question answering and interactive decision-making.
* The original paper demonstrated the approach on tasks including HotpotQA, FEVER, ALFWorld, and WebShop.

## Quick Memory

```text
Reason and Plan → Think first, then create a plan
ReAct → Reason → Act → Observe → Repeat
Reasoning → Decide what to do
Action → Do something
Observation → Check what happened
```
