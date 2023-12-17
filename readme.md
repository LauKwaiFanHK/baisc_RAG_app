# Retrieval-Augmented-Generation (RAG)

## Some foundational concepts
### Large language models (LLM)
- Pre-trained neural network to respond to human queries.
- Size of the neural network is characterised by number of parameters it contains.
- LLM parameters are settings that you can adjust to control how the LLM generate texts. They affect the quality, diversity and creativeity of the generated texts. Some popular parameters are temperature, number of tokens, top-p etc.

## What is RAG?
- A technique to enhance the accuracy and reliability of LLMs by accessing and fetching relevant information from external sources.
- RAG theoretically reduces a model's hallucination (i.e. a model make a wrong guess).
- RAG is a way to retrain a model (or create a custom model) by linking to knowledge bases that contain additional, new datasets. This allows user to have conversations with data repositories.

## How RAG works?
<img src="/images/NVIDIA-RAG-diagram-scaled.jpg">

1. Create a machine-readable index of a knowledge base that contains your customized data (i.e. a vector store)
2. Create embedding (or a vector): convert a user query into a machine-readable numeric format. This numeric version of the query is called an embedding or a vector.
3. Compare the embedding (or vector) to vectors in the vector store (An embedding model will do this job).
4. When there is a match or multiple matches, retrieve the relevant data.
5. Convert these relevant data into human-readable words and pass them back to the LLM.
6. LLM combines the retrieved words and its own response to the query into a final human-readable answer. Present the answer to the user.

[Details description of above steps here](https://blog.langchain.dev/tutorial-chatgpt-over-your-data/)

## References:
- [What Is Retrieval-Augmented Generation, aka RAG?](https://blogs.nvidia.com/blog/what-is-retrieval-augmented-generation/)
- [Tutorial: ChatGPT Over Your Data](https://blog.langchain.dev/tutorial-chatgpt-over-your-data/)