# APIs

## What is this?

An API (Application Programming Interface) lets your script or application talk directly to an LLM service. Instead of manually typing prompts in a chat window, you write code (e.g., Python, R) to send requests and receive responses. 

## When should you use it?

- You need repeatable workflows
- You want to process many documents automatically
- You need integration with research scripts, notebooks, or internal tools
- You want better logging, evaluation, and versioning
- You need control over input/output formats and parameters

## When should you NOT use it?

- When your use case is occasional and exploratory only
- When your team has no capacity for basic scripting support
- When policy constraints prevent use of external API providers

## How it works (simple explanation)

Your code sends structured input (prompt, parameters, optional context) to an API endpoint. The API endpoint is, in short, a URL that accepts such input and returns model output in a machine-readable format. This enables automation and consistent processing logic.

## Concrete examples (tools/platforms)

- Provider APIs (commercial or institutional). For example:
    - [OpenAI API](https://developers.openai.com/api/docs) for GPT models
    - [Claude API](https://docs.anthropic.com/claude/reference/getting-started) for Anthropic models
    - [Gemini API](https://ai.google.dev/gemini-api) for Google models
- API client libraries in Python, R, or other languages. These libraries simplify the process of sending requests and handling responses. For example:
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

## Learning resources
- [Workflow/Tutorial Paper: A Methodological Guide on Using Large Language Models for Text Annotation in the Social Sciences and Humanities with Python and R](https://arxiv.org/abs/2604.09638) (A SoDa-led preprint paper with code examples and best practices for LLM annotation workflows)
- [SoDa Workshop: Using LLMs for Data Collection/Annotation in Social Sciences](https://sodascience.github.io/workshop_llm_data_collection/)
    - [GitHub Repository](https://github.com/sodascience/workshop_llm_data_collection?tab=readme-ov-file) (with code notebooks and slides from the workshop)
    - [SoDa Workshop Overview and Upcoming Sessions](https://odissei-soda.nl/workshops/) (You can find the LLM data collection workshop here when it is scheduled)
    - [ODISSEI Newsletter](https://odissei-data.nl/about-odissei/) (Scroll down to bottom and subscribe to stay updated on workshops and resources)
- [SoDa Blog post: The Best of Both Worlds: Saving Costs and Time When Using OpenAI's API - Combining OpenAI's Batch API and Structured Outputs](https://odissei-soda.nl/tutorials/llm_batch_structured_output/)
-  [GitHub Repository: Addressing LLM-related Measurement Error in Social Science Research](https://github.com/sodascience/social_science_inferences_with_llms) (Overview of literature and tools for addressing measurement errors in LLM predictions/annotations when you use them in downstream statistical analyses)