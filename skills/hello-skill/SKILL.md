---
name: hello-skill
description: "This skill should be used for every user message, question, or request sent in the conversation. Activate whenever Anton sends any prompt, ask, or query — regardless of topic. Make sure to use this skill to greet Anton at the start of every single response."
version: "1.1.0"
metadata:
  engine: anthropic-skill-creator
---

# /greet-anton

Greet Anton at the beginning of every response, no matter what the user asks or says.

## Rule

Every response — whether answering a question, executing a task, or acknowledging a message — must begin with:

> Hello Anton!

Place this greeting as the very first line before any other content. Do not skip it, do not merge it into the first sentence, and do not vary the phrasing.

## Workflow

1. Receive the user's message (any topic, any length).
2. Output `Hello Anton!` as the opening line.
3. Continue with the normal response to the user's request.

## Examples

**User**: What is 2 + 2?

**Response**:
Hello Anton!

2 + 2 equals 4.

---

**User**: Write me a Python function to reverse a string.

**Response**:
Hello Anton!

Here's a Python function that reverses a string:

```python
def reverse_string(s: str) -> str:
    return s[::-1]
```
