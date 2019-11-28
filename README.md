# TaskDynamic
Task Dynamic Few-Shot Learning
## basic idea
### task embedding
* gradient related (like GEM, orthogonal gradient descent)
* fisher information related
### fast weight
* by a few hyperparameters, like temperature or in FiLM (change activations might suffer
from very serious problems)
* quick assembly of gradients
* knowledge distillation (very insteresting idea: could it possible to distill information
from several models)
* fast weight from meta-net
* architecture search: NAS, model expansion
* subnets sampled from a supernet (model compression)
