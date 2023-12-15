A basic Retrival Augmented Generation (RAG) app using jaccard similarity.

Reference tutorial: https://medium.com/@wachambers/a-beginners-guide-to-building-a-retrieval-augmented-generation-rag-application-from-scratch-e52921953a5d

Problems with jaccard similarity
- no semantic interprettion because it tries to look for words that appear in both user input and source doucument.
- output would be the same if user input is a negative statement e.g. "I am not looking for the link of carbon/react Github repository." and "I am looking for the link of carbon/react Github repository." produce the same output "carbon/react Github link: https://github.com/carbon-design-system/carbon/tree/main/packages/react".

Conclusion: this app deals with the "Retrival" part of RAG only (large language model (LLM) is not yet incorporated in this app).

