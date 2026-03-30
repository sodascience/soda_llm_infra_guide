# Chat interface

## What is this?

A chat interface is the most direct way to use a large language model (LLM): you type a prompt and receive a response in a conversational window, similar to tools like ChatGPT.

---

## When should you use it?

- Early idea generation  
- Drafting and rewriting text  
- Quick coding support and debugging hints  
- Fast exploration of a research topic before formal analysis  

---

## When should you NOT use it?

- When you need strict reproducibility or traceability of outputs  
- When you must automate repeated tasks at scale  
- When your workflow requires integration with scripts or datasets  
- When governance policies restrict data entry into external services (unless using an institutional chat tool; see `../institutional-resources/chat-interface.md`)  

---

## How it works (simple explanation)

You provide instructions in natural language. The model generates a response by predicting the most likely continuation of text given your input and prior context.

The interface manages conversation history for you, but typically hides system-level instructions and offers limited control over model parameters, tools, and backend infrastructure.

---

## Concrete examples (tools/platforms)

- Public chat assistants (e.g., ChatGPT-like tools)  
- Institution-provided chat tools (where available)  
- Enterprise chat interfaces with governance and access controls  

---

## Example workflow (step-by-step)

1. Define your immediate goal (e.g., summarize three papers).  
2. Write a prompt including context, constraints, and expected output format.  
3. Iterate with follow-up prompts to refine structure and accuracy.  
4. Verify key claims against original sources.  
5. Save effective prompts for reuse (e.g., in shared notes or templates).  

---

## Pros and cons

| Pros | Cons |
|---|---|
| Fastest way to start | Limited control over automation and configuration |
| Low technical barrier | Outputs are difficult to reproduce exactly |
| Strong for brainstorming and writing support | Limited traceability of decisions and prompts |
| No setup required | Risk of fluent but incorrect outputs |

---

## Typical users

- Researchers new to LLMs  
- Students and research assistants preparing drafts  
- Domain experts needing occasional coding or writing support  