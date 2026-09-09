## 4. Observation vs. Reflection

**Definition:** Observation tells the agent **what happened**, while reflection helps the agent understand **what to do about it**.

**Example:**

```text
Observation:
"Payment failed."

Reflection:
"The payment did not succeed, so I should try another payment method."
```

**Instructions:**

* Observation should focus on facts and results.
* Reflection should focus on meaning and the next decision.
* Keep the two steps conceptually separate.
* Use both to avoid continuing with outdated or incorrect information.

## 5. Complete Multi-Step Example

**Definition:** A multi-step agent can use observation and reflection after each action to understand results and adjust its plan.

**Example:**

```text
Goal:
"Find the cheapest laptop under $800."

Step 1 — Reason
I need to find laptops that cost less than $800.

Step 2 — Act
Search an online store for laptops under $800.

Step 3 — Observe
Results:
- Laptop A → $750
- Laptop B → $820
- Laptop C → $700

Step 4 — Reflect
Laptop B is over the budget.
Laptop C is currently the cheapest option.
I should check another store before deciding.

Step 5 — Act
Search another store for the same laptops.

Step 6 — Observe
Results:
- Laptop A → $720
- Laptop C → $680

Step 7 — Reflect
Laptop C is cheaper than the previous results.
The current lowest price is $680.

Step 8 — Act
Select Laptop C at $680.

Step 9 — Final Result
"The cheapest option I found is Laptop C for $680."
```

**Instructions:**

* After each action, observe the result before continuing.
* Reflect on whether the result supports the current plan.
* Change the plan when new information requires it.
* Continue the loop until the goal is completed.

## Quick Memory

```text
Observation → What happened?
Reflection → What does it mean?
Memory Update → What should I remember?
Agent Loop → Reason → Act → Observe → Reflect → Repeat
```
