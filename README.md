# LLMs-Lab-2024

This repository contains projects, research, and educational resources focused on Large Language Models (LLMs).

## 1. Task-oriented Dialogue System

   This demo implements a multi-turn, task-oriented intelligent customer service system using the OpenAI API.
   
## 2. Function-Calling

This folder contains various demos showcasing the capabilities of Function Calling.

### Function Calling Demos

   - **`POI`**:  
     This demo uses Amap's (Gaode Map) public API to retrieve information about hotels, restaurants, attractions, and other points of interest (POIs) near a specific location. It allows querying nearby POIs relative to a given point.

   - **`SQL`**:  
     This demo demonstrates how Function Calling handles sophisticated database tasks and generates SQL queries.

   - **`Stream`**:  
     This demo showcases examples of Function Calling in Stream mode.


## 3. RAG

This folder contains two different **RAG (Retrieval-Augmented Generation)** pipelines. The first one is based on Elasticsearch (ES), and the second one is based on a vector database, ChromaDb.

## Offline Steps

```mermaid
graph TD;
    A[Document Loading] --> B[Document Splitting]
    B --> C[Vectorization]
    C --> D[Insert into Vector Database]

graph TD;
    E[Receive User Query] --> F[Vectorize User Query]
    F --> G[Retrieve from Vector Database]
    G --> H[Populate Prompt Template]
    H --> I[Call LLM with Final Prompt]
    I --> J[Generate Response]

## Offline Steps

![Offline Steps](path/to/offline_steps.png)

## Online Steps

![Online Steps](path/to/online_steps.png)


### Pipelines

- **`run_RAG_vector_database_pipeline`**:  
  RAG Pipeline based on ChromaDb Vector Database.

- **`run_RAG_ES_pipeline`**:  
  RAG Pipeline based on Elasticsearch (ES).
