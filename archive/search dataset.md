creating a search ranking and retrieval database is expensive. the number of samples in such a dataset is (# queries) X (# documents). This is unfeasable to label by hand. Better would be to generate a "silver" dataset by using teacher models. These models can be expensive to run, but are only used offline. The results of these models can then be used as labels. Next sections will explore some teacher pipelines

## Cross encoders
use cross encoders for the retrieval and ranking step. This assumes the cross encoder is competent enough for the ground truth.


## LLM relevance judges
use a system prompt to let an llm be the judge of the relevance for a query document pair. Here is an example of such a prompt:
```
you are an assessor in a panel to review search result relevancy. You will need to review query-document pairs in the form of query:<>, document:<>. The scores you should give are 4: perfect match, 3: relevant, 2: good, 1: somewhat relevant and 0: not relevant at all. Only answer with 4,3,2,1 or 0.
```
 
using multiple llms can be used to somewhat average out the noise. [[ranking metrics#ERR (Expected Reciprocal Rank)|Exponential normalization]] could be used to be compatible with the [[#Cross encoders]] technique
## Query augmentation
Modify keyword searches with natural language. For example Liability -> Is this a liability clause? or "What does a liability clause look like?". This grows the number of queries.
