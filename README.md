![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)
![Vertex AI](https://img.shields.io/badge/Powered%20by-Vertex%20AI-FF6F00.svg)

# 📄 Multimodal Retrieval Augmented Generation (RAG) using the Gemini API in Vertex AI

This project shows how to use Google Cloud's **Vertex AI**, **Gemini 2.0 Flash API**, and other technologies for managing text and image-based documents to create a **Multimodal Retrieval-Augmented Generation (RAG)** system. Using the Gemini paradigm, the solution is designed to extract, search, compare, and reason about documents that contain text and images (tables, charts, and graphs).

![May 5, 2025, 03_08_01 AM](https://github.com/user-attachments/assets/68e2dc6b-bf2e-4a71-84a6-983d9f209ec5)

---
## 🚀 Key Features

- Multimodal search and retrieval from documents (text and images)
- Metadata extraction and embedding generation
- Gemini 2.0 Flash model integration for intelligent reasoning
- Comparative image reasoning
- Fully automated in a Google Cloud Vertex AI Workbench notebook

---

## 🧰 Requirements

Make sure you have the following packages installed in your environment:

```bash
google-cloud-bigquery==3.25.0
google-cloud-pipeline-components==2.15.0
google-cloud-aiplatform==1.59.0
pandas==2.2.2
kfp==2.7.0
numpy>=1.22.4,<2.0.0
matplotlib==3.8.0
langchain==0.3.8
torch==2.1.0
tensorflow==2.17.0
pymupdf
rich
colorama
```


## 📓 Setup Instructions

### 🔧 Task 1: Open the Notebook in Vertex AI Workbench

1. In the Google Cloud Console, go to the **Navigation menu**.
2. Click on **Vertex AI > Workbench**.
3. Find your **Workbench instance name** and click the **Open JupyterLab** button.
4. The JupyterLab interface will open in a new browser tab.

---

### 📦 Task 2: Set Up the Notebook

1. Open the provided notebook file.
2. When prompted, select **Python 3** from the list of available kernels.
3. Run the **Getting Started** and **Import Libraries** sections.
4. Set the following variables in the notebook:
   - `Project ID`: your Google Cloud **Project ID**
   - `Location`: your Google Cloud **Region**

---

### 🤖 Task 3: Use the Gemini Flash Model

1. Load the **Gemini 2.0 Flash** model (`gemini-2.0-flash`) in the notebook.
```
text_model = GenerativeModel("gemini-2.0-flash")
multimodal_model = GenerativeModel("gemini-2.0-flash")
multimodal_model_flash = GenerativeModel("gemini-2.0-flash")
```
3. Download the helper functions (`intro_multimodal_rag_utils.py`) to simplify the workflow.
4. Retrieve sample documents and images from Google Cloud Storage.

---

### 🗂 Task 4: Build Metadata of Documents

1. Use a modified version of the **Google-10K** report (14 pages).
2. Extract and store metadata from documents containing both text and images (e.g., tables, charts, graphs).

---

### 🔍 Task 5: Text Search

1. Input a simple **text query** (e.g., “net income per share”).
2. Perform search using **text embeddings**.
3. Display relevant snippets and images from the document.

---

### 🖼 Task 6: Image Search

1. Provide an **image as a query** (e.g., a revenue table).
2. Find and return similar images from the dataset using image embeddings.

---

### ⚖️ Comparative Reasoning

1. Input a query comparing two visuals (e.g., stock performance charts).
2. Use Gemini to reason over both and generate an analytical response.
3. Understand which stock performed better and why.

---

### 🤝 Task 7: Multimodal Retrieval Augmented Generation (RAG)

1. Submit a **text query** that requires both textual and visual context.
2. Retrieve:
   - Related text chunks (like in Task 5)
   - Related images (like in Task 6)
3. Combine results into `context_text` and `context_images`.
4. Use Gemini to generate an answer using this context.
5. Print the final response and **cite** the text and image sources used.

---

### 🎉 Congratulations

You've successfully built a **Multimodal RAG system** using Vertex AI and Gemini! You've:

- Extracted metadata from text and images
- Performed semantic search with text and image queries
- Compared visuals for reasoning
- Used Gemini to generate multimodal answers

### Resources:

- [Google Cloud Vertex AI](https://cloud.google.com/vertex-ai)
- [Multimodal Retrieval Augmented Generation (RAG) using the Gemini API in Vertex AI Lab](https://www.cloudskillsboost.google/focuses/85643?catalog_rank=%7B%22rank%22%3A5%2C%22num_filters%22%3A0%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=45168885)
- [Python Vertex AI SDK (google-cloud-aiplatform)](https://pypi.org/project/google-cloud-aiplatform/)

#### 📬 Let’s Connect
Have feedback, questions, or want to contribute? Feel free to reach out or fork the project!

<a href="https://www.linkedin.com/in/mansi-more-0943/"> ![LinkedIn Profile](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white) </a>

<sub>© 2025 Google LLC.</sub>


