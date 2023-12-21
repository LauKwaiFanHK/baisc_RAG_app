# Embeddings

## definition
- An embedding is a numerical representation of an information. This numerical representation is called a vector which is composed of a list of floating point numbers. 
- The distance between two vectors measures the relatedness between the information. 
- Small distance means two information is highly related while large distance means two information is not likely related.
- Therefore, embedding is understood as a representation of the semantics (meaning) of the information. Embedding is used to measure how two information matches semantically.
- Depends on the embedding API offers by a service, an information can be in the form of text, document, image, audio etc. 
- The following table summarizes how different use cases are enabled using embeddings:

| Use case | Embedding usage |
| -- | -- |
|Search | Rank the search results by relevance to a user query. |
|Clustering | Group the information by similarity. |
|Recommendations | Recommend information (e.g. products) that are highly related. |
|Anomaly detection | Identify information (i.e. outliers) that has exceptionally low relatedness. |
|Classification | Classify information that has the highest similarity label. |

## This project
- In this project, the open-source library [Sentence Transformers](https://www.sbert.net/index.html) are used to generate embeddings from sample text.
- The model [all-MiniLM-L6-v2](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2) from Sentence Transformers is used. This model
    - is trained using a [self-supervised contrastive learning objective](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2#background) that given a sentence from the pair, the model should predict which sentence out of a set of randomly sampled other sentences was actually paired with it in the dataset.
    - [Training data](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2#training-data) includes texts from Reddit comments, Yahoo answers, Stack Exchange etc.
    - hence, maps sentences and paragraphs to a 384 dimensional dense vector space.
    - intended use case is given an input text, output a vector which captures the semantic information of that input.
    - **NOTE: input text longer than 256 word pieces is truncated.** 
    - can be used for information retrieval, clustering, semantic search, sentence similarity tasks.

## References
- [What are embeddings?](https://platform.openai.com/docs/guides/embeddings/what-are-embeddings)
- [Getting Started With Embeddings](https://huggingface.co/blog/getting-started-with-embeddings)
- [Use cases and code samples of embeddings](https://platform.openai.com/docs/guides/embeddings/use-cases)