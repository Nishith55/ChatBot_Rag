# LLM Chatbot RAG Assistant

This project implements a chatbot using Retrieval-Augmented Generation (RAG) with a large language model (LLM) and LangChain. The chatbot supports general interactions with the LLM and allows users to upload PDF files to ask questions related to the content of those PDFs.

## Features

- **General Chat**: Interact with the LLM for general queries.
- **PDF Upload and Query**: Upload PDFs and ask questions based on the content of the PDFs.

## Installation

To set up the project, follow these steps:

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/Sahil-v05/ChatBot_Rag.git
   cd ChatBot_Rag

2.**Install Dependencies**:

  Create a virtual environment (optional but recommended):

  python -m venv venv
  source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

  Install the required packages:
  ```bash
  pip install -r requirements.txt
  ```

**Running the Application**

**Local Environment**
Ensure you have a GPU available to use the gemma-2-2b-it model.To use a different model or quantize the model, replace the model name in model.py and uncomment the quantization code.

Run the Streamlit application:
streamlit run streamlit_app.py

**Google Colab**
1.Select a T4 GPU runtime in Google Colab for free use of gpu.
2.Run the following commands in a Colab cell to start the Streamlit app and expose it via Serveo:

 ```bash
 !nohup streamlit run "/content/app.py" --server.port <Any_port_number> &
 !ssh -o StrictHostKeyChecking=no -o ServerAliveInterval=60 -R 80:localhost:<Any_port_number> serveo.net
```

This will open a public URL where you can access the Streamlit app.


**Usage**

1.Upload PDFs: Use the file uploader in the sidebar to upload PDF files.
2.Ask Questions: Enter your questions in the chat input field. The chatbot will respond based on the uploaded  PDF content or general knowledge.







