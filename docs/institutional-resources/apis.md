# APIs (institutional)

## What is this?

Institutional API access provides programmatic LLM usage through services connected to university or national research infrastructure and governance processes.

## How it works (simple explanation)

You request institutional API access, receive credentials, and connect your scripts or applications to approved LLM endpoints. Usage is typically monitored and governed under institutional terms.

## Concrete examples (tools/platforms)

- [SURF AI Hub / WiLLMa (pilot phase)](https://servicedesk.surf.nl/wiki/spaces/WIKI/pages/219086851/AI-Hub+WiLLMa+Pilot+phase)

### Pilot versus production: why it matters

- **Pilot services** may have changing limits, eligibility, and support scope.
- **Production services** usually provide stronger stability, support guarantees, and clearer long-term planning.
- Researchers should confirm service maturity before embedding APIs in critical workflows.

## Example workflow (step-by-step)

1. Confirm your institution participates in the relevant service pathway.
2. Review eligibility and onboarding requirements.
3. Request API access through institutional or SURF channels.
4. Build a small script to test prompts and response handling.
5. Implement logging and quality checks before scaling.
6. Reassess service maturity (pilot status, quotas, roadmap) regularly.

## Pros and cons

| Pros | Cons |
|---|---|
| Better alignment with institutional governance | Access process can take longer than public API signup |
| Supports automation and reproducibility | Pilot services may have changing conditions |
| Potentially improved trust and policy clarity | Feature set may be narrower than commercial platforms |