# Q&A Rag Pipeline

## What it does
- extracts text and images from a WebMD article about migraines*
- utilizes different retrievers (control, AutoMergingRetriever, BM25Retriever, and QueryFusionRetriever) to develop query engines for the LLM
- leverages the `meta-llama/llama-3.1-8b-instruct` LLM with detailed prompts to answer questions from a list* based on the article and generate thorough answers, as well as additional paraphrased questions for more coverage
- evaluates performance using the following metrics: faithfulness, relevancy, MRR, hit rate, precision, and recall

## Setup
- in order to use the LLM, an `.env` file must exist with the value `OPENROUTER_API_KEY=<your-api-key>`
- `WebMD.pdf`*, a pamplet of text and images relating to migraine causes and treatment that will be used for evaluation
- `my_questions.txt`*, list of sample questions that the model will try to paraphrase and answer

## Output
After all the cells are run, `results.csv` will be saved to the this directory with the questions and each retriever's answer as well as faitfulness and relevancy scores. This will also be printed along with the aforementioned metrics when the last cell is run.



*Note: additional files available on request; cannot be posted publically for academic integrity reasons
