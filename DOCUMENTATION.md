For this project, I started two approaches:

1. Multimodal Embeddings:
Initially, I considered using AWS Titan embeddings, which have shown superior performance. However, due to access limitations for personal use, I shifted to OpenAI's CLIP. Unfortunately, I encountered numerous dependency conflicts while working with CLIP.

2. Multimodal LLM for generating image summary:
My second approach involved extracting images and text using Optical Character Recognition (OCR) techniques. Given the unstructured nature of our data, extracting individual images proved challenging. I experimented with various tools like PyMuPDF, PyPDF, and Tesseract, but none provided satisfactory results.
Ultimately, I devised a workaround:
a) Convert the PDF pages into image.
b) Use a multimodal Large Language Model (LLM) to generate a comprehensive summary of the PDF(image).
c) Convert this summary into embeddings.
d) Build a retriever based on these embeddings.


In this project, I have used gpt-4o as the multimodal LLM for creating summaraies and inference LLM. For embeddings i have used text-embedding-ada-003 and FAISS for vector store.


I felt the data was incomplete without much details of the sketches (hardly 5 lines of text was there) which would be a major drawback for simple RAG, for better domain specific task fine-tuning will be the best approach.