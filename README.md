# Vector Embeddings Examples

## Contents

 - [Vector Indexing with FAISS](elastic_tests.ipynb): Notebook that demonstrates various vector indexing and similarity search options with plain FAISS library.
 - [Vector Indexing with pgvector](pgvector_tests.ipynb): Notebook that demonstrates the vector indexing and similarity search options of pgvector extension in Postges.
 - [Vector Indexing with Elasticseach dense_vector](elastic_tests.ipynb): Notebook that demonstrates the dense_vector indexing support Elasticsearch.
 
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

# Install Jupyter
pip install jupyter

# Run Jupyter
jupyter notebook

```
