Each contract at least has 2 parties. Clauses can favor either one or the other party in varying degrees. Having a model predict who is more favored by it could result in new features:

- General contract sentiment
- Search for equivalent clauses which favor the client more
- pinpoint the most unbalanced clauses
- ...

## Data strategy

## based on the back and forth between the parties:

- model predicts evaluation per clause
- document score is the sum of these evaluations
- assume a score in favor of the initiating party over the whole document
- swing the score to the other side with each iteration
	- reduce the swing size to end at 50-50
- the swing is mostly due to the changed clauses?
- **additional idea:** Clauses that did not change should keep their eval
- **Question** How to distinguish the parties
	- score is function of party embedding and clause embedding?
		- how to create party embedding?
	- Conditioning Vector?
	- depends on the model?
- **Question** Multiple parties


## Teacher student
Use llm to label the data![[Clause advantage analysis 2024-07-03 16.55.40.excalidraw]]