# ASK-MSC Data Embeddings generator

- It generate embeddings using OpenAIEmbeddings and then saves it to pinecone database
- The embeddings is then used by the ask-msc AI to answer queries

## Setting Environment variables

- Rename `.env.example` to `.env`
- Inside `.env` replace xxxxxxx with corresponding values

## Adding data

- Add the files in the data folder
- It must be a .txt file

## To generate embeddings

- run `node generate.js`

## To Test

- run `node ask.js`

## Current Bug

- When running the generate script twice the embeddings in the pinecone duplicates, it should only create embeddings for new data
- Possible Solution:
  - creating a script that only generate embeddings for the new data added, and ignores all the previously added data
  - delete all the generated data in the pinecone, and add all the new data (this solution is not efficient)
