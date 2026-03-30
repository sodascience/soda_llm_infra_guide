# Remote deployment (institutional)

## What is this?

Institutional remote deployment gives researchers access to VMs or VREs through university or national research infrastructure channels, rather than unmanaged personal cloud setups.

## When should you use it?

- You need more control than chat or API-only access
- You need team-level environments with policy oversight
- You need scalable compute but with institutional governance

## When should you NOT use it?

- When local tools are sufficient
- When your project cannot support environment management overhead
- When your timeline cannot accommodate institutional provisioning lead times

## How it works (simple explanation)

You request access to remote compute resources through your institution or SURF-linked services. After approval, you deploy code and data to the environment and run workflows under governed conditions.

## Concrete examples (tools/platforms)

- SURF Research Cloud
- University-provided VMs
- University-supported VRE platforms

## Example workflow (step-by-step)

1. Clarify project requirements (data class, model size, expected workload).
2. Select a suitable institutional remote environment.
3. Apply for access through institutional channels.
4. Configure environment, storage, and user permissions.
5. Deploy scripts or notebooks and validate on a small dataset.
6. Scale gradually while monitoring usage and policy compliance.

## Pros and cons

| Pros | Cons |
|---|---|
| Better governance alignment than ad hoc personal cloud use | Provisioning may be slower than self-service cloud |
| Flexible compute for team projects | Requires operational discipline |
| Useful stepping stone before HPC | Resource limits can constrain heavy workloads |

## Typical users

- Research groups moving beyond local execution
- Projects needing controlled collaboration spaces
- Teams balancing flexibility with institutional compliance
