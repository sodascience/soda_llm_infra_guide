# APIs

## What is this?

An API (Application Programming Interface) lets your script or application talk directly to an LLM service. Instead of manually typing prompts in a chat window, your code sends requests and receives responses.

## When should you use it?

- You need repeatable workflows
- You want to process many documents automatically
- You need integration with research scripts, notebooks, or internal tools
- You want better logging, evaluation, and versioning

## When should you NOT use it?

- When your use case is occasional and exploratory only
- When your team has no capacity for basic scripting support
- When policy constraints prevent use of external API providers

## How it works (simple explanation)

Your code sends structured input (prompt, parameters, optional context) to an API endpoint. The service returns model output in a machine-readable format. This enables automation and consistent processing logic.

## Concrete examples (tools/platforms)

- Provider APIs (commercial or institutional)
- [LangChain](https://www.langchain.com/) in Python for pipeline orchestration
- [ellmer](https://ellmer.tidyverse.org/) in R for conversational and prompt workflows in data science contexts

## Example workflow (step-by-step)

1. Define a single research task, such as coding open-ended survey responses.
2. Create a prompt template with clear output schema.
3. Implement a script that reads rows from your dataset.
4. Send each row to the API and parse the response.
5. Store outputs with metadata (model, prompt version, timestamp).
6. Evaluate quality on a validation subset and revise prompt/template.

## Pros and cons

| Pros | Cons |
|---|---|
| Enables automation and scale | Requires scripting and API key management |
| Supports reproducible pipelines | Cost management becomes important at volume |
| Easier integration with existing tools | Governance checks may be more complex |

## Typical users

- Data-oriented researchers
- Research software engineers
- Teams building repeatable LLM-assisted analysis pipelines
