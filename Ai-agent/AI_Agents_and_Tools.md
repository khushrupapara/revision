# AI Agents

## Quick Overview

| Name                  | Definition                                              | Example              |
| --------------------- | ------------------------------------------------------- | -------------------- |
| **AI Agent**          | An AI system that can plan, use tools, and take actions | Research agent       |
| **Tool**              | An external capability an agent can use                 | API, database        |
| **Memory**            | Stores information for future steps                     | Conversation history |
| **Human-in-the-Loop** | A person reviews important actions                      | Approving a payment  |

---

## 1. AI Agent

**Definition:** An AI agent is a system that **understands a task, chooses actions, uses tools, checks results, and continues until the task is completed**.

**Example:**

```text
User Request
     ↓
AI Agent
     ↓
Choose Tool
     ↓
Take Action
     ↓
Check Result
     ↓
Next Action / Complete
```

**Instructions:**

* A chatbot mainly responds to users.
* An agent can **plan and take actions**.
* Agents should have limits and safeguards for important actions.

---

## 2. Tools

**Definition:** Tools give an AI agent the ability to interact with external systems.

**Example:**

```text
Search API → Find information
Database   → Read/write data
Email API  → Send email
```

**Instructions:**

* Give agents only the tools they need.
* Limit tool permissions.
* Monitor important tool actions.

---

## 3. Memory

**Definition:** Memory allows an agent to retain useful information across steps or interactions.

**Example:**

```text
User preference
      ↓
Agent Memory
      ↓
Used in future response
```

**Instructions:**

* Store only useful information.
* Manage context carefully.
* Avoid keeping unnecessary sensitive data.

---

## 4. Human-in-the-Loop

**Definition:** A human reviews or approves important actions before they are executed.

**Example:**

```text
Agent → Prepare payment
          ↓
      Human Approval
          ↓
       Execute
```

**Instructions:**

* Use approval for high-risk actions.
* Keep an audit trail.
* Provide a way to stop the agent.

---

## 5. MCP

**Definition:** **Model Context Protocol (MCP)** is a standard for connecting AI agents to external tools and data sources.

**Example:**

```text
AI Agent → MCP → Database
                → API
                → File System
```

**Instructions:**

* MCP connects agents to tools.
* Control which tools an agent can access.
* Apply authentication and permissions.

---

## 6. A2A

**Definition:** **Agent2Agent (A2A)** is a protocol designed to allow AI agents to communicate and collaborate with other agents.

**Example:**

```text
Agent A → Agent B → Agent C
Research    Analysis    Report
```

**Instructions:**

* Useful for multi-agent systems.
* Define clear responsibilities between agents.
* Validate information passed between agents.

---

## Quick Memory

```text
AI Agent          → Think + Act
Tools             → Give capabilities
Memory            → Remember information
Human-in-the-Loop → Human approval
MCP               → Agent → Tools
A2A               → Agent → Agent
```

> **Note:** Agent capabilities, protocols, and implementation details vary between platforms.
