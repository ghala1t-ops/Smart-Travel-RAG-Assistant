# Smart Travel RAG Assistant

A Retrieval-Augmented Generation (RAG) based travel assistant for multimodal travel planning in Saudi Arabia.

The system combines flight data and Haramain High-Speed Railway train data to recommend travel routes based on cost, duration, crowd level, and carbon impact.

## Project Overview

Travel planning can be difficult when users need to compare different transportation options across separate data sources. This project solves that problem by combining flight and train datasets into one intelligent assistant that can answer travel-related questions and suggest suitable routes.

The assistant uses a hybrid RAG architecture to retrieve relevant travel information, generate valid flight-train route combinations, and produce grounded answers based on the available dataset.

## Main Features

- Flight and train data integration
- Multimodal route generation
- Cheapest route recommendation
- Fastest route recommendation
- Low-carbon route recommendation
- Train crowding analysis
- Peak travel pattern analysis
- Grounded answer generation using retrieved evidence
- Interactive Gradio interface

## System Architecture

The system includes four main stages:

1. Data preparation  
2. Retrieval  
3. Route construction  
4. Response generation  

The travel records are converted into text documents, embedded using SentenceTransformer models, stored in a FAISS vector index, and retrieved based on user queries.

## Technologies Used

- Python
- Pandas
- FAISS
- SentenceTransformers
- BAAI/bge-small-en-v1.5
- all-MiniLM-L6-v2
- Groq API
- Llama 3.1 8B Instant
- Gradio
- Jupyter Notebook

## Dataset

The project uses two transportation datasets:

- Flight dataset: around 1,810 records
- Train dataset: around 1,350 records

Additional connected-route documents were created by combining compatible flight and train trips.

## Evaluation Results

The system was evaluated using retrieval performance, route-generation accuracy, and answer quality.

Key results:

| Metric | Score |
|---|---:|
| Mean Precision@10 | 0.800 |
| Mean Recall@10 | 0.318 |
| Mean Reciprocal Rank | 0.857 |
| Structured route pass rate | 1.000 |
| Mean answer quality score | 1.000 |
| Overall internal evaluation score | 0.792 |

## Limitations

- The system uses a static dataset.
- It does not support real-time prices, delays, cancellations, or seat availability.
- Route planning is mainly limited to Makkah and Madinah.
- The current system processes English queries only.
- The generation component depends on external API availability.

## Future Work

- Connect the system to real-time flight and train APIs
- Add Arabic language support
- Expand Haramain Railway station coverage
- Improve evaluation using human feedback
- Fine-tune embeddings on Saudi transportation data
- Improve route-ranking using user feedback

## Authors

- Rahaf Jelan
- Ghala Salman
- Shahad Alzahrani

## Course

CCAI 435 Deep Learning  
Final Deep Learning Project
