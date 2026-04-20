# Remote deployment

## What is this?

Remote deployment means running LLM workloads on external compute infrastructure instead of your local machine. Common options include virtual machines (VMs) and Virtual Research Environments (VREs).

---

## When should you use it?

- Your local machine is not powerful enough  
- You need shareable environments for a team  
- You need a controlled but flexible compute setup  
- You want to avoid the overhead of HPC but need more than local resources  
- You want to test models before scaling to HPC  
- You want to transition from local prototyping to more scalable environments  

---

## When should you NOT use it?

- When your workload is small and can run locally  
- When governance rules prohibit the selected provider  
- When your team cannot maintain remote environments  
- When you need very large models requiring multi-GPU or HPC-scale infrastructure  

---

## How it works (simple explanation)

You provision remote compute, connect securely (e.g., via SSH or browser), install the required tools, and run inference or fine-tuning tasks there. Data and compute remain within the remote environment.

Depending on the setup:
- VMs are typically **persistent** (you manage them over time)  
- VREs are often **ephemeral or semi-managed** (sessions may reset or be preconfigured)  

---

## Concrete examples (tools/platforms)

### Virtual machines (VMs)

- [Exoscale](https://www.exoscale.com/): European cloud provider with VM instances  
- [AWS EC2](https://aws.amazon.com/ec2/): on-demand cloud virtual machines  
- [Google Cloud Compute Engine](https://cloud.google.com/compute): scalable VM infrastructure  
- [Microsoft Azure Virtual Machines](https://azure.microsoft.com/en-us/services/virtual-machines/): enterprise cloud VM platform  

### Virtual Research Environments (VREs)

- [Google Colab](https://colab.research.google.com/): managed notebook environment (free tier with limitations)  
- Azure ML notebooks: managed notebook environments within Azure  
- [JupyterHub](https://jupyter.org/hub): institution-hosted multi-user notebook server  
- [Binder](https://mybinder.org/): temporary environments (no GPU, limited for LLM use)  
- Institution-provided notebook environments (see [INSTITUTIONAL RESOURCES/Remote deployment](../institutional-resources/remote-deployment.md))  

### VM versus VRE: key difference

- **VM**: full control over the machine, operating system, and installed services. More flexibility, but more responsibility.  
- **VRE**: managed research workspace with preconfigured tools and interfaces. Less control, faster onboarding.  

---

## Example workflow (step-by-step)

1. Select VM or VRE based on required level of control.  
2. Create or request access to the environment.  
3. For VMs, configure access (e.g., SSH keys, firewall rules).  
4. Install runtime dependencies (Python, libraries, models).  
5. Upload or mount data.  
6. Run scripts or notebooks for inference or experimentation.  
7. Monitor usage, logs, and costs.  

---

## Typical SSH workflow for VMs

1. Generate or load your SSH key pair.  
2. Add your public key to the VM configuration.  
3. Connect using `ssh user@host`.  
4. Use tools like `tmux` or `screen` for long-running jobs.  
5. Keep scripts version-controlled for reproducibility.  

---

## Pros and cons

| Pros | Cons |
|---|---|
| More compute flexibility than local setups | Ongoing cost and operational overhead |
| Suitable for team collaboration | Requires setup of security and access controls |
| Good balance between control and usability | Risk of configuration drift without automation |

---

## Learning resources
- [SSH tutorial by DigitalOcean](https://www.digitalocean.com/community/tutorials/ssh-essentials-working-with-ssh-servers-clients-and-keys): practical SSH basics  
- [vLLM documentation](https://docs.vllm.ai/en/stable/): scalable inference on remote GPUs