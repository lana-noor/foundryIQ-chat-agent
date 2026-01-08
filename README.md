# FoundryIQ

## What this notebook is
`FoundryIQ.ipynb` is a setup notebook that shows how to create and register **Azure AI Search** knowledge sources (search indexes + blob sources) and then compose them into a **Knowledge Base** used for grounded Q\&A.

## Quick setup
1. Create a `.env` file using `.env-sample`.
2. Fill in at least:
   - `AAIS_ENDPOINT` (your Azure AI Search endpoint)
   - `AAIS_KEY` (admin key)
   - `AZURE_STORAGE_ACCOUNT_CONNECTION_STRING` (if running blob knowledge sources)
   - `PROJECT_ENDPOINT` (your AI Foundry project endpoint)
3. Run the notebook cells top-to-bottom.

## Key concepts
- **FoundryIQ**: This repo’s sample “agent + knowledge” experience. It’s meant to demonstrate building a Foundry-style assistant that can answer questions using indexed data (not just a chat model).
- **Knowledge base**: A named resource that defines *how answers are produced* (instructions + retrieval behavior) and *which sources to retrieve from*. The model’s response is grounded on retrieved content.
- **Knowledge source**: A specific connected source of data used for retrieval (for example: an Azure AI Search index, or a blob container ingested into an index). Multiple knowledge sources can be attached to one knowledge base.

## Notes
- The notebook uses the Azure AI Search Python SDK and expects your resources (indexes/containers) to exist and the credentials in `.env` to be valid.
