# Temperature & Sampling Parameters

## Quick Overview

| Name            | Definition                               | Example |
| --------------- | ---------------------------------------- | ------- |
| **Temperature** | Controls the randomness of the output    | `0.7`   |
| **Top P**       | Controls the probability range of tokens | `0.9`   |
| **Top K**       | Controls the number of possible tokens   | `10`    |

---

## 1. Temperature

**Definition:** Controls how predictable or random the model's output is.

**Example:**

```text
0.1 → More predictable
0.7 → Balanced
1.0+ → More creative (if supported)
```

**Instructions:**

* Use low temperature for consistent and predictable results.
* Use higher temperature for creative tasks.
* Higher temperature may produce more unexpected or incorrect output.

---

## 2. Top P

**Definition:** Controls the probability range of tokens that the model can choose from.

**Example:**

```text
Top P = 0.9
→ Consider tokens within the top 90% probability mass.
```

**Instructions:**

* Lower Top P → Fewer token choices.
* Higher Top P → More token choices.
* Usually adjust Temperature or Top P rather than both at the same time.

---

## 3. Top K

**Definition:** Controls the number of most likely tokens that the model can choose from.

**Example:**

```text
Top K = 3
→ Choose from the 3 most likely tokens.
```

**Instructions:**

* Lower Top K → Fewer choices.
* Higher Top K → More choices.
* `Top K = 1` → Only the most likely token is considered.
* Not all AI models support Top K.

---

## Quick Memory

```text
Temperature → How random?
Top P       → How much probability?
Top K       → How many choices?
```

> **Note:** Available settings and supported ranges depend on the AI model.

---

# Frequency Penalty & Presence Penalty

## Quick Overview

| Name                  | Definition                                               | Example |
| --------------------- | -------------------------------------------------------- | ------- |
| **Frequency Penalty** | Reduces repetition of tokens that have already appeared  | `0.5`   |
| **Presence Penalty**  | Encourages introducing tokens that have not appeared yet | `0.5`   |

---

## 1. Frequency Penalty

**Definition:** Reduces the chance of repeating the same tokens multiple times. Higher values generally reduce repetition.

**Example:**

```text
Low:  0.0 → More repetition
High: 1.0 → Less repetition
```

**Instructions:**

* Use a higher value when the output is too repetitive.
* Use a lower value when repetition is useful or natural.
* Too much penalty can make the text sound unnatural.

---

## 2. Presence Penalty

**Definition:** Encourages the model to introduce **new topics or tokens** instead of repeatedly using ones that have already appeared.

**Example:**

```text
Low:  0.0 → Stay closer to existing topics
High: 1.0 → Encourage new topics
```

**Instructions:**

* Use a higher value for brainstorming and diverse ideas.
* Use a lower value when you want the model to stay focused.
* Too much penalty can make the output less coherent.

---

## Quick Memory

```text
Frequency Penalty → Reduce repetition
Presence Penalty  → Encourage new topics
```

> **Note:** Supported ranges and behavior can vary between AI models and APIs.

---

# Stopping Criteria in LLMs

## Quick Overview

| Name                       | Definition                                      | Example                      |
| -------------------------- | ----------------------------------------------- | ---------------------------- |
| **Max Tokens**             | Limits how many tokens can be generated         | `max_tokens = 500`           |
| **Stop Sequence**          | Stops generation when a specific string appears | `"\n\n"`                     |
| **Semantic Stopping**      | Stops when the task is logically complete       | End of an answer             |
| **Streaming Interruption** | Stops generation using custom application logic | Stop after detecting `<END>` |

---

## 1. Max Tokens

**Definition:** Sets a maximum limit on how many tokens the model can generate.

**Example:**

```text
max_tokens = 500
→ Generation stops after the limit is reached.
```

**Instructions:**

* Prevents unnecessarily long responses.
* Too small a limit may cut off the response.
* The exact parameter name can vary between APIs.

---

## 2. Stop Sequence

**Definition:** A custom string that tells the model to stop generating when that sequence is produced.

**Example:**

```text
stop = ["<END>"]
→ Generation stops when <END> appears.
```

**Instructions:**

* Useful for structured or delimited output.
* The model must generate the exact sequence.
* Not all models or APIs support stop sequences.

---

## 3. Semantic Stopping

**Definition:** Stops generation when the response has **completed the required task**.

**Example:**

```text
Task: "Write one paragraph."
→ Stop when the paragraph is complete.
```

**Instructions:**

* Useful for context-dependent generation.
* Usually requires application-side logic.
* More difficult to implement reliably.

---

## 4. Streaming Interruption

**Definition:** Stops generation while tokens are being streamed based on custom application logic.

**Example:**

```text
if token == "<END>":
    stop_generation()
```

**Instructions:**

* Useful when you need real-time control.
* Can stop unwanted or excessive output.
* Requires streaming support and application logic.

---

## Quick Memory

```text
Max Tokens          → Maximum length
Stop Sequence       → Stop at specific text
Semantic Stopping   → Stop when task is complete
Streaming           → Stop using custom logic
```

> **Note:** Stopping methods and parameter names vary between AI models and APIs.

---

# Max Length in LLMs

## Quick Overview

| Name                    | Definition                                             | Example                   |
| ----------------------- | ------------------------------------------------------ | ------------------------- |
| **Max Length**          | Limits the maximum amount of text a model can generate | `500 tokens`              |
| **Max Output Tokens**   | Common parameter name for limiting generated tokens    | `max_output_tokens = 500` |
| **Prompt Instructions** | Tells the model the desired response length            | `Write in 100 words`      |
| **Stop Sequence**       | Stops generation when specific text appears            | `"<END>"`                 |

---

## 1. Max Length

**Definition:** Sets the maximum number of **tokens** the model can generate in a response.

**Example:**

```text
Max Length = 500 tokens
→ The model can generate up to 500 output tokens.
```

**Instructions:**

* Smaller limits → Faster and shorter responses.
* Larger limits → Longer and more detailed responses.
* A limit that is too small may cut off the response.
* Choose the limit based on the task.

---

## 2. Prompt Instructions

**Definition:** You can ask the model to produce a specific length without using a hard token limit.

**Example:**

```text
"Summarize this in 100 words."
```

**Instructions:**

* Useful when you want an approximate length.
* Be specific about words, sentences, or bullet points.
* This does not always guarantee an exact length.

---

## 3. Stop Sequence

**Definition:** A predefined string that tells the model to stop generating when it appears.

**Example:**

```text
Stop: "<END>"
→ Generation stops when <END> is produced.
```

**Instructions:**

* Useful for structured or delimited output.
* The model must produce the specified sequence.
* Support varies between AI models and APIs.

---

## Quick Memory

```text
Max Length     → Maximum output size
Prompt         → Desired output size
Stop Sequence  → Where to stop
```

> **Note:** Different AI providers may use different parameter names, such as `max_tokens`, `max_output_tokens`, or `max_completion_tokens`. The exact limits also vary by model.
