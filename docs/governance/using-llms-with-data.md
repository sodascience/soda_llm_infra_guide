# Using LLMs with your data

## Why this matters

Large language models (LLMs) process the text you provide. Depending on the tool you use, that data may:

- be sent to external providers  
- be logged or stored  
- be used for monitoring or improvement  
- leave your institutional environment  

Choosing the wrong setup can lead to **privacy risks, policy violations, or loss of control over your data**.

---

## Key question

> Can I use this LLM setup with my data?

The answer depends on **what data you have** and **which tool you use**.

---

## Step 1: Classify your data

### 🟢 Low-risk data (generally safe)

- Publicly available text  
- Published open-access papers  
- Synthetic or generated data  
- Non-sensitive notes or drafts  

Typically safe to use with any LLM usage mode.

---

### 🟡 Medium-risk data (use caution)

- Internal documents  
- Unpublished research  
- Draft manuscripts  
- Project notes or meeting summaries  

Recommended:
- institutional tools (chat/API)  
- controlled environments (VM/VRE/HPC)  

Avoid:
- pasting into public tools without checking policies  

---

### 🔴 High-risk data (restricted)

- Personal data (e.g., names, emails, identifiable individuals)  
- Sensitive personal data (e.g., health, political views)  
- Confidential or proprietary data  
- Restricted datasets (e.g., administrative data such as CBS data)  

Do NOT use:
- public chat tools  
- public APIs  

Use instead:
- institutional infrastructure  
- secure environments  
- HPC or controlled research platforms  

---

## Step 2 — Understand the tool you are using

### Public chat tools
(e.g., ChatGPT-style interfaces)

- Easy to use  
- Data may leave your institution  
- Limited control  

Use only for low-risk data  

---

### Public APIs
(e.g., OpenAI-style APIs)

- Programmatic access  
- More control than chat tools  
- Still external providers  

Suitable for low- to medium-risk data (if allowed)  

---

### Institutional tools (chat/API)

- Provided or approved by your university or SURF  
- Governed usage and access  
- Often preferred for research  

Suitable for:
- medium-risk data  
- sometimes higher-risk data (depending on setup)  

---

### Remote environments (VMs / VREs)

- More control over environment  
- Data handling depends on provider  
- Can be configured for privacy  

Suitable for:
- medium-risk data  
- some sensitive data (if properly configured)  

---

### HPC / secure environments

- Strict access control  
- Data stays within controlled infrastructure  
- Designed for sensitive or large-scale workloads  

Required for:
- high-risk or restricted data  

---

## Rule of thumb

> If you would not email the data to an external service, do not share it with a public LLM (including APIs).

---

## Common mistakes

- Copy-pasting sensitive data into public chat tools  
- Assuming “research use” automatically allows data sharing  
- Ignoring institutional policies  
- Using APIs without checking where data is processed  
- Forgetting to log or document LLM usage  

---

## Good practices

- Check your institution’s AI or data policy  
- Prefer institutional tools when available  
- Use local or controlled environments for sensitive work  
- Remove or anonymize personal data where possible  
- Keep track of:
  - model used  
  - prompts  
  - parameters  
- Validate outputs against original data  

---

## When in doubt

If you are unsure:

- Contact your research support or IT services  
- Check institutional AI guidance  
- Use a more restrictive setup (e.g., institutional or local)  

---

## Summary

| Data type | Recommended tools |
|----------|-----------------|
| Low-risk | Any (chat, API, local, remote) |
| Medium-risk | Institutional tools, VMs/VREs |
| High-risk | HPC, secure environments only |