# HPC

## What is this?

HPC (High-Performance Computing) uses powerful shared clusters to run compute-intensive workloads that exceed normal workstation or small VM capacity.

## When should you use it?

- You need to run large batches of LLM experiments
- You need high-memory or multi-GPU jobs
- You need parallel evaluation across many datasets or prompts
- You are fine-tuning models or running large-scale benchmarking

## When should you NOT use it?

- For quick exploratory prompting
- For tiny workloads that run well on local or small cloud setups
- When your team cannot maintain job scripts and queue-based workflows

## How it works (simple explanation)

You submit jobs to a scheduler, usually as batch scripts. The scheduler places your job in a queue and runs it when requested resources become available.

## Concrete examples (tools/platforms)

- University HPC clusters
- National HPC resources with GPU partitions
- Scheduler tooling such as Slurm

## Example workflow (step-by-step)

1. Prepare a reproducible environment (modules, container, or environment file).
2. Write a batch script with CPU/GPU, memory, and time requests.
3. Submit the job with Slurm commands.
4. Track queue status and logs.
5. Validate outputs and rerun with tuned parameters if needed.
6. Archive results and job metadata for reproducibility.

## Batch jobs and Slurm basics

- Batch jobs are non-interactive scripts submitted for queued execution.
- Slurm is a common scheduler for requesting and managing resources.
- Typical actions include submit, monitor, cancel, and inspect job logs.

## Pros and cons

| Pros | Cons |
|---|---|
| Handles large-scale and parallel workloads | Steeper learning curve than chat or API use |
| Access to high-end compute and storage | Queue times can delay iteration |
| Strong fit for reproducible batch pipelines | Requires planning and resource estimation |

## Learning resources