Currently, no training data is available, no training infra is available. Cloud is an option

# Proposal:

- Training Data in s3
- Model Data in s3
- Training in (GPU) containers [[cloud gpu providers]]
	- dl data from s3 or read from disk
- inference: 
	- EKS if the gpu instances are cheaper than sagemaker
	- target cpu if possible
	- sagemaker: bring your own image
	- fastapi, grpc, async or node application?
	- use onnx-runtime
	- 