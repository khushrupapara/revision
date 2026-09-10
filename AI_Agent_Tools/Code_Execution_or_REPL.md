# Code Execution / REPL

## Quick Overview

| Name           | Definition                                                        | Example                               |
| -------------- | ----------------------------------------------------------------- | ------------------------------------- |
| Code Execution | Allows an AI agent to write and run code to solve a task.         | Running Python to calculate data      |
| REPL           | A loop that reads code, runs it, shows the result, and continues. | Testing Python code interactively     |
| Sandbox        | An isolated environment where code can run with limited access.   | E2B sandbox                           |
| Code Agent     | An AI agent that can write, execute, and check code.              | Agent that analyzes data using Python |

## 1. Code Execution

**Definition:** Code execution allows an AI agent to write and run code instead of only generating text.

**Example:**

```text
User: Calculate the average of 10, 20, and 30.

Agent:
1. Writes Python code.
2. Runs the code.
3. Gets the result: 20.
4. Returns the answer.
```

**Instructions:**

* Use code execution for calculations, data processing, and other tasks that are easier to solve with code.
* The agent can inspect the execution result and use it to continue its task.
* Python is commonly used because it has many useful libraries.
* Always review generated code before using it in sensitive environments.

## 2. REPL

**Definition:** REPL stands for **Read-Eval-Print Loop**. It reads code, executes it, displays the result, and repeats the process.

**Example:**

```text
Read  →  Evaluate  →  Print  →  Repeat

2 + 3
→ 5

5 * 4
→ 20
```

**Instructions:**

* REPLs are useful for quickly testing small pieces of code.
* Results are available immediately after execution.
* Errors can be detected and fixed step by step.
* A REPL is different from a full application build because code is executed interactively.

## 3. Sandbox

**Definition:** A sandbox is an isolated environment where code can run with restricted access to the host system.

**Example:**

```text
AI Agent
   ↓
Generates Python Code
   ↓
Sandbox
   ↓
Runs Code Safely
   ↓
Returns Result
```

**Instructions:**

* Run AI-generated code inside a sandbox when possible.
* Restrict access to files, network resources, and system operations.
* Use resource and execution limits to reduce risk.
* A sandbox improves safety, but it should not be treated as automatically risk-free.

## 4. Code Agent

**Definition:** A code agent is an AI agent that can write code, execute it, handle errors, and use the results to complete a task.

**Example:**

```python
from praisonaiagents import Agent

agent = Agent(
    name="code-runner",
    instructions="Write and execute Python to answer questions."
)

agent.start("Calculate the average of 10, 20, and 30.")
```

**Instructions:**

* Give the agent a clear task and execution goal.
* Let the agent use a sandboxed interpreter for code execution.
* Check execution errors and results before continuing.
* Keep the execution environment limited to the tools and packages the agent needs.

## Quick Memory

```text
Code Execution → Write and run code
REPL → Read → Run → Print → Repeat
Sandbox → Isolated environment for safer execution
Code Agent → AI that writes and executes code
```

```
from praisonaiagents import Agent

agent = Agent(
    name="code-runner",
    instructions="Write and execute Python to answer questions."
)

agent.start("Calculate the average of 10, 20, and 30.")
```
