# Ai summary

## Current LN service
code in henchman/lit spikes/aisum
docs on 
- [requirements for create+dms](https://confluence.lexisnexis.dev/display/HEN/Ai+Summary)
- [rag ai summarizer LN](https://confluence.lexisnexis.dev/pages/viewpage.action?spaceKey=CHAT&title=RAG+Summarization+API) -> not sufficient for our usecase, need to develop prompt anyway, why not leverage llm directly to better control timings

## Privacy Concerns
private data could b contained in the document, so the docs should be handled with care with regards to LLM services 

| service | used by|
| ------- | -------|
|three way classifier||
|gene's classifier||
|lsa entity extraction||
|citation finder||
|;||
