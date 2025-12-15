# Milestone 1 — YouTube Video to Text (Transcript Extraction)

## Objective
Build a reliable pipeline that converts a YouTube lecture video into clean, readable text.

This milestone focuses **only** on transcript extraction and preprocessing.  
No AI models. No summarization. No frontend.

## What You Need to Build

A Python script or notebook that:

1. Accepts a YouTube video URL as input
2. Extracts the transcript using `youtube-transcript-api`
3. Handles:
   - Manual captions
   - Auto-generated captions
   - Language fallback (prefer English)
4. Cleans the transcript:
   - Removes timestamps
   - Merges text segments in correct order
   - Normalizes whitespace and punctuation
5. Saves the output in two formats:
   - Plain text (`.txt`)
   - Raw transcript data (`.json`)

## Folder Structure

Milestone 1/
├── transcript_extractor.py # or transcript_extractor.ipynb
└── outputs/
├── <video_id>.txt
└── <video_id>.json
