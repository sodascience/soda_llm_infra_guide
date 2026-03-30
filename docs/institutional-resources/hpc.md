# HPC (institutional)

## What is this?

Institutional HPC access provides large-scale compute through university clusters and national resources such as Snellius (SURF), typically for workloads that exceed standard remote environments.

## When should you use it?

- You need substantial GPU/CPU resources
- You need many parallel experiments or large benchmarking runs
- You need robust storage and job scheduling at scale

## When should you NOT use it?

- For lightweight exploratory prompting
- When small-scale cloud or local options already meet needs
- When your project cannot support batch-job workflow practices

## How it works (simple explanation)

You obtain project access, then submit jobs to shared cluster resources. Scheduling systems allocate resources based on quotas, policies, and queue availability.

## Concrete examples (tools/platforms)

- University HPC clusters
- Snellius (SURF national supercomputer)
- Slurm-based scheduling environments

## Example workflow (step-by-step)

1. Assess whether your workload justifies HPC scale.
2. Discuss options with local research support or HPC coordinators.
3. Apply for access (institutional pathway, project request, or grant-linked process).
4. Prepare reproducible batch scripts and environments.
5. Run pilot jobs, then scale to larger batches.
6. Monitor quotas, storage, and queue behavior to plan efficiently.

## When to scale up to Snellius or similar national resources

- Local university cluster capacity is insufficient
- Multi-GPU or high-memory jobs exceed local limits
- Project timelines require large parallel throughput
- National support and shared expertise offer better fit

## How access works (grants, quotas)

- Access often combines institutional entitlement and project-level allocation.
- Some pathways are quota-based; others depend on proposal or grant mechanisms.
- Clear planning for compute hours, storage, and expected outputs improves approval success.

## Pros and cons

| Pros | Cons |
|---|---|
| Enables national-scale compute and advanced workloads | Onboarding and queue systems require learning |
| Better fit for large or long-running experiments | Access can depend on quotas or proposal cycles |
| Strong support ecosystem in Dutch research infrastructure | Not ideal for very rapid ad hoc iteration |

## Typical users

- Advanced computational research teams
- Projects with explicit scaling requirements
- Consortia working across institutions in the Netherlands
