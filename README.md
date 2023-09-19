# IBM Generative AI Cookbooks

This repository contains a number of jupyter notebooks to help you get up and running with IBM Generative AI (Watsonx.AI)

## Contents

### Retrieval Augmented Generation (RAG)
 - [RAG 1.0](notebooks/rag-1.0-vectordb.ipynb): Simple extractive single-turn question answering, leveraging vector databases.
 - [RAG 1.1](notebooks/rag-1.1-vectordb.ipynb): Simple extractive single-turn question answering, leveraging vector databases. Focusing on long-form extractive question answering.

## Running the cookbooks locally

It's always good practice to use a virtual environment when running python whether it be a script or a notebook. These instructions will walk you through setting up a jupyter notebook virtual environment:

_Note_: You will need to have [Git Large File Storage (git-lfs)](https://git-lfs.com/) installed

```bash
# Clone the Repository
git clone git@github.ibm.com:james-sutton/ibm-generative-ai-cookbooks.git

# Change directory
cd ibm-generative-ai-cookbooks

# Pull large files from git-lfs
git lfs install
git lfs pull

# Create your virtual environment
python -m venv .venv

# Activate the Virtual environment
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run Jupyter
jupyter notebook

```

### Your .env file

Because these cookbooks interact with services running in the IBM Cloud, you will need to save your API keys in a .env file for the notebooks to use. An example file ([`.env.example`](.env.example)) is a good template to copy. Add the relevant credentials to this and save it simply as `.env` inside the top level of the project.

### Poetry (alternative)

If you like to use poetry, or if you are developing these notebooks, you can follow these instructions instead. Make sure you have [Poetry](https://python-poetry.org/) and [git-lfs](https://git-lfs.com/) installed.


```bash
# Clone the Repository
git clone git@github.ibm.com:james-sutton/ibm-generative-ai-cookbooks.git

# Change directory
cd ibm-generative-ai-cookbooks

# Pull large files from git-lfs
git lfs install
git lfs pull

# Create a Poetry virtual environment
poetry shell

# Install dependencies
poetry install

# Run Jupyter
poetry run jupyter notebook

```

## Development instructions

To make merging and management of notebooks an easier task, there are some useful development tools that should be used if contributing:

### Pre-commit
When you first pull down this repository run the following command to install the pre-commit hook: `pre-commit install`

From now on, when you commit changes to your branch (or if you run `pre-commit run`). All staged files will be checked for python code style as well as stripping out notebook results. Additionally, an updated `requirements.txt` file will be generated making the install process easy for users.

By making pull requests into the `develop` branch with no output in the notebooks, it's much easier to diff them to see what the code changes are.

Once the code in the `develop` branch is ready to be released, a build can take place which will execute the notebooks and commit the full output versions to the `main` branch. 

