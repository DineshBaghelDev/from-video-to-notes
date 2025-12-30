# Milestone 2 — Build a Robust Summarization Engine

## Objective

Implement a **working text summarization pipeline** that can reliably summarize long-form text (YouTube transcripts / articles) while respecting transformer context limits.

## Problem Statement

Most transformer-based summarization models (T5, BART) cannot process long documents directly.

Your system must:

1. Accept long input text (>10,000 characters)
2. Break it into valid chunks
3. Summarize each chunk
4. Combine the results into a final coherent summary

## Functional Requirements

### 1. Model Usage

* Use **any Hugging Face summarization model**

  * Examples: `t5-small`, `bart-large-cnn`
* Must use `transformers` library

### 2. Chunking Engine (Mandatory)

* Implement a chunking function
* Constraints:

  * Chunk size ≤ model context window
  * Overlap between chunks to preserve context

Recommended:

* Chunk size: 800–1400 characters
* Overlap: 100–200 characters

### 3. Hierarchical Summarization

Your pipeline must follow this structure:

1. Split text → chunks
2. Summarize each chunk independently
3. Merge intermediate summaries
4. Generate final summary from merged text


## Deliverables

### Required

* Python script or notebook implementing the pipeline
* Functions:

  * `chunk_text(text)`
  * `summarize_chunk(chunk)`
  * `final_summarize(chunks)`

### Output

* Input: long transcript text
* Output:

  * Intermediate chunk summaries
  * Final clean summary


## Bonus (Optional)

* Compare two models (T5 vs BART)
* Add sentence-aware chunking
