# HPC

## What is this?

HPC (High-Performance Computing) refers to shared computing clusters designed to run large-scale, compute-intensive workloads that exceed the capacity of local machines or small virtual machines.

These systems typically consist of many interconnected nodes (CPUs/GPUs) managed by a scheduler, allowing users to run jobs in parallel at scale.

---

## When should you use it?

- You need to run large batches of LLM experiments  
- You need high-memory or multi-GPU jobs  
- You need parallel evaluation across many datasets or models  
- You are fine-tuning models or running large-scale benchmarking  
- You need reproducible, large-scale pipelines  

---

## When should you NOT use it?

- For quick exploratory prompting  
- For small workloads that run well locally or on a VM  
- When your workflow requires real-time interaction  
- When your team cannot maintain job scripts and queue-based workflows  

---

## How it works (simple explanation)

You submit jobs to a scheduler (commonly Slurm) using batch scripts. The scheduler queues your job and executes it when the requested resources become available.

- **Jobs / batch scripts**: Non-interactive scripts specifying what to run and required resources  
- **Scheduler**: Software (e.g., Slurm) that manages job submission, scheduling, and execution  
- **Queue**: A waiting line where jobs are held until resources become available; priority may depend on policies or quotas  
- **Resources**: Requested compute such as CPUs, GPUs, memory, runtime, and number of nodes  

---

## Concrete examples (tools/platforms)

### Academic and national HPC
- University HPC clusters  
- National infrastructure such as SURF (e.g., Snellius)  

See [INSTITUTIONAL RESOURCES/HPC](../institutional-resources/hpc.md) for more.

### Commercial HPC (HPC-as-a-Service)

- [AWS (EC2 + ParallelCluster)](https://aws.amazon.com/hpc/) — scalable HPC clusters with GPU support  
- [Microsoft Azure HPC](https://azure.microsoft.com/en-us/solutions/high-performance-computing/) — GPU clusters with high-speed interconnects  
- [Google Cloud HPC](https://cloud.google.com/hpc) — distributed workloads with GPUs/TPUs  
- [Oracle Cloud Infrastructure (OCI) HPC](https://www.oracle.com/cloud/hpc/) — HPC with low-latency networking  
- [OVHcloud HPC](https://www.ovhcloud.com/en/bare-metal/uc-high-performance-computing/) — European HPC and GPU clusters (GDPR-friendly option)  

---

## Example workflow (step-by-step)

1. Prepare a reproducible environment (modules, container, or environment file).  
2. Write a batch script specifying CPU/GPU, memory, and time requirements.  
3. Submit the job via the scheduler (e.g., `sbatch`).  
4. Monitor job status and logs.  
5. Validate outputs and iterate with adjusted parameters.  
6. Archive results, logs, and configuration for reproducibility.  

---

## Pros and cons

| Pros | Cons |
|---|---|
| Handles large-scale and parallel workloads | Steeper learning curve than chat or API use |
| Access to high-end compute and storage | Queue times can delay iteration |
| Strong fit for reproducible batch pipelines | Requires planning and resource estimation |
| Enables multi-GPU and distributed workloads | Less suitable for interactive exploration |

---

## Learning resources

### Batch jobs and Slurm basics
- https://carpentries-incubator.github.io/hpc-intro/ — excellent beginner-friendly HPC tutorial
- https://slurm.schedmd.com/documentation.html — official Slurm documentation  

### Running LLM workloads on HPC
- [Accelerate](https://huggingface.co/docs/accelerate/index) — This Hugging Face Accelerate documentation provides a practical guide to scaling PyTorch-based workflows from local machines to distributed environments such as multi-GPU servers, cloud instances, or HPC clusters. It introduces a lightweight abstraction (`Accelerator`) that allows researchers to run the same code across different hardware setups with minimal changes, while handling device placement, parallelism, and mixed precision under the hood. The documentation also includes a range of tutorials and how-to guides covering both beginner and advanced topics for training and inference, such as the [Distributed Data Parallel tutorial](https://pytorch.org/tutorials/intermediate/ddp_tutorial.html) and [DeepSpeed integration](https://huggingface.co/docs/accelerate/usage_guides/deepspeed).
- [vLLM](https://docs.vllm.ai/en/latest/) — library for scalable LLM inference (often used on HPC clusters)  

### Environment management and reproducibility
- [docker](https://docs.docker.com/) — containerization for consistent environments  
- [apptainer](https://apptainer.org/docs/) — HPC-friendly containers (formerly Singularity)  

### HPC knowledge bases
- [HPC-Wiki](https://hpc-wiki.info/hpc/) 
- [Princeton Research Computing](https://researchcomputing.princeton.edu/support/knowledge-base)
