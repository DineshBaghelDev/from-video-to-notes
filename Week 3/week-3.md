
# Week 3 — Frontend & Backend

## Goal
Learn how to:

* Build a clean UI for an AI project
* Connect frontend with ML logic
* Handle user input, loading states, and outputs
* Deploy a usable demo 


## Why Streamlit?
* Zero frontend overhead
* Fast prototyping
* Industry-accepted for ML demos, hackathons, MVPs

## Core Video Resources 

### **1. Streamlit Crash Course**
  [https://youtu.be/o8p7uQCGD0U?si=lCI4FkR0im2rZzmo](https://youtu.be/o8p7uQCGD0U?si=lCI4FkR0im2rZzmo)

### **2. Streamlit + FastAPI**
  [https://youtu.be/SR5NYCdzKkc?si=5zQAFBOUnlzJqL0V](https://youtu.be/SR5NYCdzKkc?si=5zQAFBOUnlzJqL0V)


## Official Documentation
### Streamlit Docs

* Main docs
  [https://docs.streamlit.io/](https://docs.streamlit.io/)

* Widgets reference
  [https://docs.streamlit.io/library/api-reference/widgets](https://docs.streamlit.io/library/api-reference/widgets)

* Layouts & containers
  [https://docs.streamlit.io/library/api-reference/layout](https://docs.streamlit.io/library/api-reference/layout)


## What You Must Learn for This Project
### 1. Input Handling

* text area (manual input)
* file upload (TXT / transcript)
* YouTube URL input (later)

Relevant docs:

* `st.text_area`
* `st.file_uploader`
* `st.text_input`


### 2. Output Rendering

* clean summary display
* bullet points
* expandable sections

Widgets:

* `st.write`
* `st.markdown`
* `st.expander`


### 3. Loading & Feedback (Critical UX)

Never freeze the UI.

Learn:

* `st.spinner`
* progress indicators
* status messages


### 4. Project Structure (Non-Negotiable)

You should move away from single-file chaos.

Example:

```
app.py
summarizer/
 ├── model.py
 ├── chunking.py
 └── pipeline.py
utils/
 └── helpers.py
```

Frontend **must not** contain ML logic directly.



