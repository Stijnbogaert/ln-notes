
Decoupling layer between +ai orchestrator and:
- search engines 
- embedding services

Currently deployed as lambda (python runtime)
need to write the handler to map between opensearch fields and eqas fields

  

Q

Sync embedding model and stored embeddings?

- abstracted behind content type

is EQAS sufficient for draff/ask

- EQAS + Opensearch are both needed, but sufficient together
- also needs answer finder

  

  

to follow up

- Full document chunking and embedding
- where does the answer finder fit in