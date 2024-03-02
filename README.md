# Question-Answering Pipeline with VectorDB and Large Language Models (LLM)

## Overview:

Welcome to the Question-Answering Pipeline with VectorDB and Large Language Models (LLM). This project aims to create an efficient and scalable pipeline for question-answering tasks using [ChromaDB](https://www.trychroma.com/) which is an open-source vector database, in conjunction with [Llama2](https://llama.meta.com/) which is also an open-source Large Language Model (LLM).

### Workflow:

1. **User Input:** Users provide textual data sources in formats such as .pdf. These documents serve as the basis for generating responses.

2. **Document Loading:** [LangChain](https://www.langchain.com/)'s document loader is employed to efficiently load and preprocess the provided documents, ensuring compatibility with downstream tasks.

3. **Document Chunking:** The loaded documents are divided into smaller, manageable chunks to enhance the efficiency of the question-answering process.

4. **Embedding Storage in VectorDB (ChromaDB):** The chunks' embeddings are generated and stored in ChromaDB, VectorDB's underlying technology, enabling fast and accurate information retrieval.

5. **Query Processing:** User queries are converted into embeddings, allowing for a seamless comparison with the stored document embeddings.

6. **Vector Database Search:** The VectorDB is queried with the generated embeddings to retrieve relevant chunks of information, optimizing the question-answering process.

7. **LLM Processing ([Llama2](https://llama.meta.com/)):** The retrieved embeddings are passed to [Llama2](https://llama.meta.com/), an LLM, which generates context-aware and accurate answers to user queries.

## Getting Started

To kickstart the Question-Answering Pipeline, users need to provide their textual data sources in supported formats (Currently Supported format are: **pdf, csv, html, xlsx, docx, xml, json**). Follow the next section to ensure proper installation and configuration of dependencies.

## How to Run Guide

Follow these steps to run the Question-Answering Pipeline successfully:

1. **Install Dependencies:** Ensure that you have all the required dependencies installed. Run the following commands in a notebook cell:

    ```
    !pip install langchain
    !pip install PyPDF
    !pip install sentence_transformers
    !pip install chromadb
    !pip install accelerate
    !pip install bitsandbytes
    !pip install jq
    !pip install unstructured
    ```

2. **Customize Parameters:**

    Open the notebook and locate the following parameters:
    - ***jq_schema:*** Customize this parameter according to your data schema. Define the structure of your textual data for proper loading and processing.

    - ***input_path:*** Specify the path to your textual data source, such as a .pdf file. Ensure that the path is correctly set to your document.

3. **Hugging Face Authorization Token:** Make sure to obtain an authorization token from Hugging Face for downloading the [Llama2](https://llama.meta.com/) model. This token is crucial for accessing the model. Set the token in the appropriate section of the notebook.

4. **Run the Notebook:** Run the Jupyter notebook cell by cell. Ensure that each cell executes successfully without errors.

## Contributions

We welcome contributions and feedback from the community. Whether you identify issues, have suggestions for improvements, or want to extend the functionality, your input is valuable to us. Feel free to contribute to the project. Thank you for exploring our Project.