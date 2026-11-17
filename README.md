# Build a RAG API with FastAPI

**Project Link:** [View Project](https://nextwork.ai/projects/d7ecb20f-0096-430f-8ad5-65f081720bcd)

**Author:** Yash Mugalikar

---

## Introducing Today's Project!

In this project, I'm going to build a RAG pipeline using FastAPI and ChromaDB This will help me understand how RAG works I'm interested in this because I would like to know more about AI and would like to have a better understanding about it both passionately and professionally.

### Key tools and concepts

The key tools I used include FastAPI, ChromeDB, Ollama and SwaggerUI.\
Key concepts I learnt include RAG, embeddings and metadata filtering.

### Challenges and wins

This project took me approximately 1 hr.\
The most challenging part was embeddings.

## Performing RAG Manually

In this step, I'm going to do a manual RAG demo to understand RAG

RAG stands for-\
\*Retrieval\
\*Augmented\
\*Generation

![Performing RAG Manually](https://nextwork.ai/merry_beige_smart_weka/uploads/d7ecb20f-0096-430f-8ad5-65f081720bcd_v3j7x5b9)

### Understanding the three parts of RAG

I performed RAG manually by being giving the prompt some personal details\
The three parts are:-\
1\. Retrieval\
2\. Augmentation\
3\. Generation

### Comparing the two AI models

The key difference I noticed is qwen2.5:0.5b is used for chats and conversations, ehilr nomic-embed-text is for semantic search.

## Building a Personal Knowledge Base

In this step, I'm going to create personal profile, chunk the text and store the embeddings in ChromeDB\
Embeddings are numericals representation of the meaning behind the text

![Building a Personal Knowledge Base](https://nextwork.ai/merry_beige_smart_weka/uploads/d7ecb20f-0096-430f-8ad5-65f081720bcd_g3h7m2r5)

### Creating the profile document

Its going to help by using my personal profile to answer questions about myself that it did not have before. We'll use RAG to give AI the personal profile.

### How semantic search finds relevant chunks

When I ask a question, ChromaDB finds the chunks whose vectors are closest in that high-dimensional space.

## Creating the RAG API with FastAPI

In this step, I'm going to build an API that rings the full RAG pipeline together.\
I'll test it using the built-in Swagger UI

![Creating the RAG API with FastAPI](https://nextwork.ai/merry_beige_smart_weka/uploads/d7ecb20f-0096-430f-8ad5-65f081720bcd_j5m1r8t2)

### How the /ask endpoint works

When a question comes in, my endpoint finds the most relevant  chunks by querying ChromeDB, this passes those to the LLM to generate a grounded response.

### Testing with Swagger UI

I tested my API by asking "What my name is?", "What is a fun fact about me?"\
The AI answered with my name, and the fun fact I provided in the personal profile text file.   \
The context used was from the said personal profile text file.

## Extending to a Multi-User AI Directory

In this project extension, I'm adding multi-user support because it allows us to add multiple personalized context based on the user behind the API

![Extending to a Multi-User AI Directory](https://nextwork.ai/merry_beige_smart_weka/uploads/d7ecb20f-0096-430f-8ad5-65f081720bcd_d5g9k3n7)

### Adding the POST /documents endpoint

In this project extension, I added a POST endpoint that allows the user to add their own profiles.\
Metadata filtering allows us to filter context based on the user.

![Extending to a Multi-User AI Directory](https://nextwork.ai/merry_beige_smart_weka/uploads/d7ecb20f-0096-430f-8ad5-65f081720bcd_r8t2w6y1)

### Verifying multi-user filtering

In this project extension, I tested multi-user queries by first using no user filter and then using the user filter\
The filter works because it only shows for the selected chunkd for the fitered user's Chunk.

## Wrapping Up

I did this project today to learn how to implement a RAG pipeline.\
Another skill I want to learn is how i can use multiple AI models.
