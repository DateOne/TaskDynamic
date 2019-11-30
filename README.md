# Task Dynamic Few-Shot Learning
## basic idea
### task embedding
* gradient related: GEM (cross product of loss gradient); Orthogonal Gradient Descent (model
loss employed to restrict new task's gradients of loss); Memory Aware Synapses
* fisher information related: Task2Vec
* auxiliary model: FiLM (directly learning a representation); Reconciling meta-learning and 
continual learning with online mixtures of tasks
* training related: MAML, proto-maml (training with support set)
* knowledge distillation: progress and compress
### fast parameters
* changing a few hyperparameters: TADAM (temperature); FiLM (affine transformation parameters);
Reconciling meta-learning and continual learning with online mixtures of tasks
* fast weight: meta-net
* subnets: missing
* quick assembly of gradients (sympathy)
* changing architecture: missing; nas; learning to grow
* knowledge distillation: progress and compress
* training related: MAML, proto-maml
### some thoughts
* task embedding: model gradient, loss gradient, fisher information; fast parameters:
changing hyperparameters; subnets (robust)
* conditional distillation
1. pseudo-code
for epoch in epoch:
  for batch in dataset:
      train model
      compute task2vec embedding (or other task embedding)
      predict some hyper-parameters
      train hyperparameter predictor
2. other methods except maml might not work
3. pseudo-code
#train
for epoch in epoch:
  for batch in dataset:
    #discrimitively training
    calculate neural network relationships with batch (how)
    discrimitively updating (how)
    #distill (as an experiment to see whether the distilled model can learn multiple 
    distributions and surpass baseline; in a common sense, it might be better)

#test
for batch in dataset:
  #distill more models (sound to be unreasonable but worth of attempt)
  calculate neural network relationships with batch (how, but same as training)
  get the output
  #or test with the distilled model
    
