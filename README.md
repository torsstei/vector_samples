# Vector Embeddings Examples

## Contents

 - [Vector Indexing with FAISS](elastic_tests.ipynb): Notebook that demonstrates various vector indexing and similarity search options with plain FAISS library.
 - [Vector Indexing with pgvector](pgvector_tests.ipynb): Notebook that demonstrates the vector indexing and similarity search options of pgvector extension in Postges.
 - [Vector Indexing with Elasticseach dense_vector](elastic_tests.ipynb): Notebook that demonstrates the dense_vector indexing support Elasticsearch.
 - [Vector embedding with OpenAI through LangChain and search in Pinecone](langchain_pinecone_embedding_tests.ipynb): Notebook that demonstrates usage of LangChain for embedding encoding with OpenAI and vector search in Pincecone.
 
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

# Set the env variables for Elastic connectivity (used in pgvector_tests.ipynb)
export PGUSER=<your PG user>
export PGPASSWORD=<your PG pw>
export PGSSLROOTCERT=<your PG certificate>

# Set the env variables for Elastic connectivity (used in elastic_tests.ipynb)
export ESUSER=<your ES user>
export ESPASSWORD=<your ES pw>
export ESHOST=<your ES hostname>
export ESPORT=<your ES port number>

# Set the env variables for OpenAI and Pinecone sign ups (used in langchain_pinecone_embedding_tests.ipynb)
export OPENAI_API_KEY=<your OpenAI API Key>
export PINECONE_API_KEY=<your pinecone API Key>
export PINECONE_ENVIRONMENT=<your pinecone tunrime environment, e.g.: "gcp-starter">
export PINECONE_INDEX=<index with 1024 dimensions>

# Install Jupyter
pip install jupyter

# Run Jupyter
jupyter notebook

```
