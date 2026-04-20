# How to use LLMs in research

Researchers can use LLMs through several pathways. These pathways differ in two key dimensions:

- **Level of control**: how much you can customize prompts, models, data flow, and deployment.
- **Technical difficulty**: how much setup and engineering effort is needed.

The practical spectrum is:

**chat -> dashboards -> APIs -> local deployment -> remote deployment -> HPC**

Moving right usually increases control and complexity.

---

## Comparison Across Usage Modes

| Mode | Control | Technical difficulty | Typical speed to start | Best for |
|---|---|---|---|---|
| Chat interface | Low | Very low | Minutes | Ideation, writing support, quick coding help |
| LLM dashboards | Low to medium | Low | Minutes to hours | Prompt testing, comparing outputs |
| APIs | Medium to high | Medium | Hours to days | Automation, integrating LLMs in research pipelines |
| Local deployment | High | Medium to high | Days | Privacy-sensitive work on manageable model sizes |
| Remote deployment | High | Medium to high | Days | Team workflows, controlled environments, larger models |
| HPC | Very high | High | Days to weeks | Large-scale experiments, parallel jobs, fine-tuning |

---

## How To Interpret The Spectrum

- If your goal is **speed and ease**, start with chat or dashboard tools.
- If your goal is **reproducibility and automation**, APIs are often the turning point.
- If your goal is **data control or model control**, local and remote deployments become relevant.
- If your goal is **scale**, HPC is typically required.

---

## Practical Decision Rules

1. Use the simplest option that meets your governance and data requirements.
2. Move to a more advanced option only when your current approach blocks research quality or scale.
3. Keep a migration path in mind: chat prompts can become dashboard experiments, then API workflows.

---

## Typical Progression In Real Projects

Many projects start with exploratory prompting in chat interfaces, then transition to structured prompt testing in dashboards, and later move to APIs for reproducible scripts. Teams handling sensitive data often shift to institutionally managed remote environments, and computationally intensive projects eventually migrate to HPC.
