# Local deployment

## What is this?

Local deployment means running an LLM on your own machine or on institution-managed hardware under your direct control, instead of relying on an externally hosted API.

## When should you use it?

- You need stronger control over data locality (e.g., sensitive data that cannot leave your machine)
- You want offline or low-latency experimentation
- You are testing smaller open models for specialized tasks
- You want to validate models before scaling to remote environments
- You have access to local hardware that can support the model size you need
- You want to avoid ongoing costs of remote compute for frequent inference

## When should you NOT use it?

- When you need very large models that exceed local hardware limits
- When cloud or institutional infrastructure is already available and policy-approved
- When you need to collaborate with a team that cannot access the same local environment
- When you want to quickly iterate without the overhead of local setup and maintenance

## How it works (simple explanation)

You install a local inference runtime, download model weights, and run prompts directly on your machine. Performance (latency, throughput) depends heavily on CPU/GPU memory and model size.

## Concrete examples (tools/platforms)
- User-friendly local LLM apps
    - [Ollama](https://ollama.com/): easy-to-use local LLM runtime with chat + API interface  
    - [LM Studio](https://lmstudio.ai/): desktop app for running and chatting with local models  
    - [Jan.ai](https://jan.ai/)： open-source local AI assistant with privacy focus  

- Inference engines (core runtime layer)
    - [llama.cpp](https://github.com/ggerganov/llama.cpp)： efficient C++ inference engine for running quantized models locally  
    - [vLLM](https://github.com/vllm-project/vllm)： high-performance inference engine for serving LLMs
    - [Text Generation Inference](https://github.com/huggingface/text-generation-inference) — production-ready LLM inference server

- Programming frameworks (research workflows)
    - [Hugging Face Transformers](https://huggingface.co/docs/transformers/index)： Python library for loading and running LLMs programmatically  

## Example workflow (step-by-step)

1. Select a model size your hardware can support.
2. Install a local inference tool and required dependencies.
3. Download model weights from a trusted source.
4. Run a baseline prompt benchmark on sample data.
5. Tune runtime settings (context length, precision, batch size).
6. Validate output quality before wider use.

## Pros and cons

| Pros | Cons |
|---|---|
| Strong data control and local execution | Limited by hardware memory and compute |
| Useful for offline experimentation | Setup and maintenance burden |
| Potentially lower long-term per-call cost | Large models may be impractical |

## Learning resources
#### Getting started (quick local setup)
- [Ollama docs](https://ollama.com/docs) — beginner-friendly way to run and manage LLMs locally  
- [llama.cpp](https://github.com/ggerganov/llama.cpp) — practical guide and examples for running LLMs locally (CPU/GPU, quantization)  

---

#### Research workflows (core libraries)
- [Hugging Face Transformers docs](https://huggingface.co/docs/transformers/index) — load models, run inference, build pipelines  
- [Hugging Face Accelerate](https://github.com/huggingface/accelerate) — manage CPU/GPU and multi-device setups  
- [Microsoft Guidance](https://github.com/microsoft/guidance) — structured prompting and controlled generation  

---

#### Serving & scaling (API-style deployment)
- [vLLM docs](https://docs.vllm.ai/en/stable/) — high-performance inference engine for scalable deployment  
- [Text Generation Inference (TGI)](https://huggingface.co/docs/text-generation-inference/index) — production-ready LLM serving  
- [Open WebUI](https://github.com/open-webui/open-webui) — self-hosted chat interface for local models  

---

#### Fine-tuning (advanced)
- [PEFT (Parameter-Efficient Fine-Tuning)](https://huggingface.co/docs/peft/index) — efficient fine-tuning methods like LoRA  
- [QLoRA](https://github.com/artidoro/qlora) — fine-tune large models on limited hardware  

---

#### Learning & fundamentals
- [DeepLearning.AI: Open-Source Models with Hugging Face](https://www.deeplearning.ai/short-courses/open-source-models-hugging-face/) — structured course on using open models locally  
- [llm.c](https://github.com/karpathy/llm.c) — minimal implementation for understanding LLM internals  




