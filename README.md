# Fine-Tuning-TinyLlama-with-QLoRA

Fine-tuned the TinyLlama 1.1B Chat model using QLoRA (4-bit LoRA adapters) on a 2k-sample subset of the Alpaca-cleaned dataset to improve instruction-following capabilities.
Developed a Colab-friendly training pipeline with gradient checkpointing and mixed-precision (fp16) to efficiently train on limited GPU resources.
Implemented evaluation using ROUGE metrics, comparing outputs of the base model and the fine-tuned model across 100 validation examples.
Achieved significant improvements in ROUGE scores:

## Model Evaluation (ROUGE Score)

| Model       | ROUGE-1 | ROUGE-2 | ROUGE-L |
|------------|---------|---------|---------|
| Base Model | 0.194   | 0.062   | 0.136   |
| Fine-Tuned | 0.322   | 0.128   | 0.222   |

**Observation:**  
The QLoRA fine-tuned TinyLlama model significantly improves instruction-following performance compared to the base model, achieving higher ROUGE scores across all metrics.

Demonstrated better instruction alignment, concise responses, and inclusion of real-world examples in generated text.
Showcased side-by-side comparison of base vs fine-tuned outputs for qualitative evaluation.

**Tech Stack & Tools**: Python, PyTorch, Hugging Face Transformers, PEFT, QLoRA, Alpaca Dataset, Evaluate (ROUGE), Google Colab.
