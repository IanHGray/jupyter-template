# jupyter-template

Template repo for jupyter notebooks, deployed through docker-compose for multi-layered applications.

Create a new template repository for non-universal changes.

## Quick Start

1. Clone this repo and run 
```
docker-compose up --build
```
2. Follow the localhost:8888 link to the jupyter server  
3. Create notebooks in the src folder, this folder is shared between your hard drive (this repo), and the docker container hosting jupyter.

## Jupyter Notebook Types

The default is pyspark, you can update the Dockerfile image to pull down any notebook: https://hub.docker.com/u/jupyter

## Local Application Additions

You can extend the docker-compose.yaml file to add application containers to the stack.  You can run apps like Redis, Postgres, Neo4j, anything with a docker image that the notebook may depend on.

## Requirements

Update requirements.txt, please _VERSION_ your packages.

## jupyter.env

Enter anything you would call os.getenv() with, it will load the environment variables into the Jupyter container _only_
