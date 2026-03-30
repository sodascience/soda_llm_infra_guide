# Remote deployment

## What is this?

Remote deployment means running LLM workloads on external compute infrastructure instead of your laptop. Common options are virtual machines (VMs) and Virtual Research Environments (VREs).

## When should you use it?

- Your local machine is not powerful enough
- You need shareable environments for a team
- You need controlled but flexible compute setup

## When should you NOT use it?

- When your workload is tiny and can run locally
- When governance rules prohibit the selected provider
- When your team cannot maintain remote environments

## How it works (simple explanation)

You provision remote compute, connect securely, install tools, and run inference or training tasks there. Data and compute stay in that remote environment.

## Concrete examples (tools/platforms)

### Virtual machines (VMs)

- AWS EC2
- Google Cloud Compute Engine

### Virtual Research Environments (VREs)

- Google Colab
- Institution-provided notebook environments

## VM versus VRE: key difference

- **VM**: full control over the machine, operating system, and installed services. More responsibility.
- **VRE**: managed research workspace with less infrastructure overhead. Less control, faster onboarding.

## Example workflow (step-by-step)

1. Select VM or VRE based on needed control.
2. Request or create the environment through your provider.
3. For VMs, configure security groups and SSH access.
4. Connect with SSH and install runtime dependencies.
5. Upload or mount data and run scripts/notebooks.
6. Monitor costs, logs, and resource usage.

## Typical SSH workflow for VMs

1. Generate or load your SSH key pair.
2. Add your public key to the VM configuration.
3. Connect from terminal using `ssh user@host`.
4. Use terminal multiplexing and versioned scripts for reliable runs.

## Pros and cons

| Pros | Cons |
|---|---|
| More compute options than local setups | Ongoing cost and operations overhead |
| Team-friendly collaboration potential | Security and governance setup required |
| Better fit for medium-to-large workloads | Risk of configuration drift without automation |

## Typical users

- Research teams with moderate engineering support
- Projects requiring custom dependencies and controlled compute
- Groups transitioning from local to scalable environments
