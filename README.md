# AI-Powered Resume Form Filler with Voice Feedback

This project is an AI-driven application that automates the process of filling out job application forms using a candidate's resume. It combines **document parsing**, **semantic search**, and **language model reasoning**, and includes a **voice feedback interface** powered by Whisper.

With support for full-page screenshot input, this tool makes it easy to fill out any job application, even if it’s not in a standard format.

⚠️ To use this project, you will need:

- **OpenAI API key** (for GPT-4 and embeddings)  
- **LlamaParse API key** (available at [llama-cloud.com](https://llama-cloud.com))
---

## 🔍 Features

- 📄 **Resume Parsing with LlamaParse**  
  Automatically extracts structured information from uploaded PDF resumes using LlamaParse and OpenAI embeddings.

- 📑 **Application Form Parsing**  
  Converts scanned PDF application forms into readable text using `pytesseract` and `pdf2image`.

- 💬 **Field Matching with GPT-4**  
  A field-by-field question-answering engine uses GPT-4 to extract answers from the resume for each required field.

- 🧠 **RAG Architecture**  
  Implements Retrieval-Augmented Generation (RAG) via a `VectorStoreIndex` for semantically querying resume content.

- 🎙 **Voice Feedback Collection**  
  Uses OpenAI Whisper and Gradio to collect and transcribe verbal feedback from the user to improve the generated answers.

---

## 🚀 How It Works

1. **Upload your resume** and a **job application form** PDF.
2. The form is parsed using Optical Character Recognition to detect the fields that need to be filled.
3. Each field is turned into a question and answered by querying the vectorized resume using GPT-4.
4. A final result is generated: a list of fields filled in with concise, factual responses.
5. Optionally, the user can provide feedback — either by typing or **speaking into the microphone**.
6. The assistant iterates based on the feedback and finalizes the form.

---

## 🛠 Tech Stack

- `Python`
- `OpenAI GPT-4`, `OpenAI Whisper`
- `LlamaParse`, `pytesseract`, `pdf2image`
- `LlamaIndex` / `VectorStoreIndex`
- `Gradio` (for voice input UI)
- `asyncio` and `event-driven` design pattern

---

## 📁 Project Folder Structure

```
├── Agent.ipynb                             # Main notebook for running the AI workflow
├── README.md                               # Project description and setup instructions
├── SemyonTsyrenov_Resume_MachineLearning   # Sample resume PDF (replaceable with any other)
├── helper.py                               # Helper functions for parsing, Optical Character Recognition, and matching
├── job_form.pdf                            # Sample application form (can be replaced with any form)
├── requirements.txt                        # Python dependencies list
```

### 🔄 Replaceable Files

- job_form.pdf
  You can replace this with any job application form (PDF or screenshot). The system will parse and extract text using Optical Character Recognition.
- SemyonTsyrenov_Resume_MachineLearning
  This is a sample resume. You can upload your own resume in PDF format to test or use the application.


