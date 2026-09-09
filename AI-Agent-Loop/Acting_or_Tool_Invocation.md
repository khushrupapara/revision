# Acting / Tool Invocation

## Quick Overview

| Name            | Definition                                                       | Example                           |
| --------------- | ---------------------------------------------------------------- | --------------------------------- |
| Acting          | The agent performs an action to make progress toward a goal.     | Searching the web for information |
| Tool Invocation | The process of calling a specific tool with the required inputs. | Calling `calculator(10, 5)`       |
| Tool            | A function that gives an AI agent an extra capability.           | Web search, calculator, database  |

## 1. Acting

**Definition:** Acting is the step where an AI agent performs an action based on its current goal and plan.

The action may involve using a tool, accessing information, or changing something in an external system.

**Example:**

```text
Goal → Find today's weather

Plan → Get current weather information

Action → Call the weather tool
```

**Instructions:**

* Choose an action that helps move toward the goal.
* Use the appropriate tool when external information or capabilities are needed.
* Provide the required inputs to the tool.
* Use the result to decide what to do next.

## 2. Tool Invocation

**Definition:** Tool invocation is the process of calling a tool and providing it with the required inputs.

The AI model typically decides **which tool to use and what arguments to provide**, while the agent or tool-calling system handles the actual execution.

**Example:**

```text
AI decides:
"I need to calculate 25 × 4."

Tool Call:
calculator(a=25, b=4)

Tool Result:
100
```

**Instructions:**

* Select the tool that matches the task.
* Provide the correct arguments and data types.
* Execute the tool call through the agent's tool system.
* Store or pass the result back to the model for the next step.

## 3. Tool Selection

**Definition:** Tool selection is choosing the most appropriate tool for the current task.

**Example:**

```text
Task → Find the current Bitcoin price

Available tools:
- Calculator
- Web Search
- Database

Selected tool → Web Search
```

**Instructions:**

* Match the tool to the task.
* Check what inputs the tool requires.
* Prefer specialized tools when they provide better or more reliable results.
* Do not use a tool when the task can be completed without it.

## 4. Acting Workflow

**Definition:** The acting workflow is the process of selecting a tool, calling it, receiving its result, and using that result for the next step.

**Example:**

```text
Goal
  ↓
Plan
  ↓
Select Tool
  ↓
Provide Inputs
  ↓
Call Tool
  ↓
Receive Result
  ↓
Use Result for Next Step
```

**Instructions:**

* The model determines what action is needed.
* The agent executes the requested tool call.
* The tool performs the actual operation.
* The result is returned to the agent/model.
* The agent can then continue reasoning or perform another action.

## 5. Complete Multi-Step Example

**Definition:** A multi-step agent task uses several actions and tool calls to complete one larger goal.

**Example:**

```text
Goal:
"Find the weather in London and decide whether an umbrella is needed."

Step 1 — Reason
The agent needs current weather information.

Step 2 — Select Tool
Choose the weather tool.

Step 3 — Invoke Tool
weather_tool(location="London")

Step 4 — Receive Result
Weather:
- Temperature: 14°C
- Condition: Rain
- Rain probability: 80%

Step 5 — Reason
There is a high chance of rain, so an umbrella is recommended.

Step 6 — Act
The agent prepares the final response.

Step 7 — Final Result
"Yes, take an umbrella. There is an 80% chance of rain in London."
```

**Instructions:**

* A single goal can require multiple reasoning and action steps.
* Each tool call should provide the inputs required by that tool.
* Use the tool result as new information for the next step.
* The agent can select another tool if the current result is not enough.
* Multi-step tasks often follow a loop: **Reason → Act → Observe → Reason → Act**.

## Quick Memory

```text
Acting → Perform an action
Tool → Extra capability
Tool Invocation → Call the tool
Tool Selection → Choose the right tool
Workflow → Select → Call → Result → Next step
Multi-Step Agent → Reason → Act → Observe → Repeat
```
