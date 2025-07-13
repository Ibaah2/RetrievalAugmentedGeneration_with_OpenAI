# RetrievalAugmentedGeneration_with_OpenAI

Project Workflow (Step-by-Step)
PDF Ingestion
Recipe books in PDF format are loaded and each page is converted into an image using a PDF-to-image conversion library.

PDF Conversion
Each PDF page is converted to an image

Base64 Extraction
Base64 is applied to each image to represent binary data (images) as plain text .

Embedding Generation
Each page is embedded using OpenAI's embedding model to create dense vector representations.

Vector Storage with FAISS
All embeddings are stored in a FAISS vector index to enable efficient similarity search.

Query Processing
A user enters a query. The query is also embedded and used to search the FAISS index for the most relevant text chunks.

Answer Generation with OpenAI
The top retrieved chunks and the user’s query are combined into a prompt and passed to OpenAI’s language model to generate a final response.

Response Output
The generated answer is returned to the user, based on the content from the ingested recipe books.
