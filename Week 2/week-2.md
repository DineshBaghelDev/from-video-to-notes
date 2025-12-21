# Week 2 — Language Model Usage & Enhanced Summarization

## Goal
Understand how to use transformer models from Hugging Face and optionally learn basics of LangChain and fine-tuning.

This week helps you build the core summarization engine using real NLP models and gives you deeper references so you can extend or optimize your pipeline later

## Video Resources

### **Core Transformer Usage**
- **Getting Started With Hugging Face in 15 Minutes**  (Recommended)
  - https://www.youtube.com/watch?v=QEaBAZQCtwE  
  (Covers transformers, pipeline, tokenizer, models — great overview)
- **How to use Hugging Face Models**  
  - https://www.youtube.com/watch?v=1h6lfzJ0wZw
    (Covers using bart-cnn/t5-small model)

- **Dealing with Long text**
  - https://www.youtube.com/watch?v=UTlb5C7xG9A


## Optional but Useful Videos

I know u want to learn more. Just making a summarizer won't make u a good ML engineer. Here are some technologies used in Industry standards.

- **LangChain Introduction (optional)**  
  - https://www.youtube.com/watch?v=nAmC7SoVLd8&t=930s  
  (Shows chaining models & workflows; useful if you want to scale logic later)

- **Fine Tuning + Using Ollama (optional)**  
  - https://www.youtube.com/watch?v=pTaSDVz0gok  
  (Good for understanding how fine-tuning works in practice)

## Official Documentation (For more Information)

### **Hugging Face Transformers**
- Main docs:  
  https://huggingface.co/docs/transformers/index

- Summarization pipeline docs:  
  https://huggingface.co/docs/transformers/main_classes/pipelines#summarization

- Model hub:  
  https://huggingface.co/models?pipeline_tag=summarization


## Handling Long Documents

Most summarization models have token limits. YouTube transcripts are much longer than these limits, so you must use chunking.

### Chunking Strategy:
1. split transcript into segments that fit model token limits  
2. add slight overlap (to preserve context)
3. summarize each segment
4. combine all summaries
5. produce a final summary of the summaries

This is called hierarchical summarization.

### Practical Example:
- chunk size: 1000–1400 characters
- overlap: 150 characters
- summarizer model: bart-large-cnn

**Never dump the full transcript into the model.
You will get random garbage.
Always chunk.**