# Vector Embeddings Examples

## Contents

 - [Vector Indexing with FAISS](elastic_tests.ipynb): Notebook that demonstrates various vector indexing and similarity search options with plain FAISS library.
 - [Vector Indexing with pgvector](pgvector_tests.ipynb): Notebook that demonstrates the vector indexing and similarity search options of pgvector extension in Postges.
 - [Vector Indexing with Elasticseach dense_vector](elastic_tests.ipynb): Notebook that demonstrates the dense_vector indexing support Elasticsearch.
 - [Use watsonx, Elasticsearch, and LangChain to answer questions (RAG)](Use%20watsonx%2C%20Elasticsearch%2C%20and%20LangChain%20to%20answer%20questions%20(RAG).ipynb): Notebook that shows a RAG pattern with LangChain using IBM WatsonX models and Elasticsearch as vector store.
 - [Vector embedding with OpenAI through LangChain and search in Pinecone](langchain_pinecone_embedding_tests.ipynb): Notebook that demonstrates usage of LangChain for embedding encoding with OpenAI and vector search in Pincecone.
 - [RAG on Slack Conversations with OpenAI and Pinecone](slacktor.ipynb): Notebook that demonstrates a RAG pattern with retrieval of slack conversations and using OpenAI LLM and Pinecone.
 - [RAG on Slack Conversations with WatsonX and ElasticSearch](slacktor.ipynb): Notebook that demonstrates a RAG pattern with retrieval of slack conversations and using WatsonX LLM and ElasticSearch in IBM Cloud.
 
## Running the notebopoks

```bash
# Clone the Repository
git clone https://github.com/torsstei/vector_samples.git

# Change directory
cd vector_samples

# Create your virtual environment
python -m venv .venv

# Activate the Virtual environment
source .venv/bin/activate

# Set the env variables for IBM Cloud and WatsonX (used in slacktor-ibmcloud.ipynb and Use%20watsonx%2C%20Elasticsearch%2C%20and%20LangChain%20to%20answer%20questions%20(RAG).ipynb)
export PROJECT_ID=<your WatsonX project ID>
export IBM_CLOUD_API_KEY=<your IBM Cloud API key>

# Set the env variables for Elastic connectivity (used in pgvector_tests.ipynb)
export PGUSER=<your PG user>
export PGPASSWORD=<your PG pw>
export PGSSLROOTCERT=<your PG certificate>

# Set the env variables for Elastic connectivity (used in all demo notebooks with Elastic)
export ESUSER=<your ES user>
export ESPASSWORD=<your ES pw>
export ESHOST=<your ES hostname>
export ESPORT=<your ES port number>

# Set the env variables for OpenAI and Pinecone sign ups (used in slacktor.ipynb and langchain_pinecone_embedding_tests.ipynb)
export OPENAI_API_KEY=<your OpenAI API Key>
export PINECONE_API_KEY=<your pinecone API Key>
export PINECONE_ENVIRONMENT=<your pinecone tunrime environment, e.g.: "gcp-starter">
export PINECONE_INDEX=<index with 1024 dimensions>

# Set the env variables for scrapting Slack conversations (used in slacktor.ipynb and slacktor-ibmcloud.ipynb)
export SLACK_API_TOKEN=<your Slack API token>
export SLACK_CHANNEL=<the name of the Slack channel from which you want to scrape conversations>


# Install Jupyter
pip install jupyter

# Run Jupyter
jupyter notebook

```
