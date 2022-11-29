Welcome!

In this project I fine-tuned different pretrained Transformers-based models to do extractive question answering, which means 
that given a passage and question regarding that passage, a part of the passage is returned as an answer.

My goal for this project was to show my knowledge of different architectures available in Transformers library and my ability of fine-tuning them to do Question Answering.

I used AdversarialQA dataset for training and validation. Each model was validated after each epoch of training with ROUGE metrics. 
Architecture that achieved the best results was trained on AdversarialQA and SQuAD 1.1 using hyperparameters from it's best training run on only AdversarialAQ.
Additional training data improved results on AdversarialQA.
