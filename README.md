# Can Robustness Against Instruction Format Be Improved Through Adversarial Training In Language Models?
This is my Dissertation, submitted in support of my BSc Computer Science & AI degree from the University of Bath, achieving a grade of 80%

Summary: A range of work has found that language models give different responses when superficial changes are made to the input (i.e. it means the same thing, but uses different words or structure). This work focuses on what happens when causal reasoning instructions are paraphrased using different paraphrase formats. It finds that training using a single format results in a brittle model, which performs well on instructions which use that format, but performs poorly when the format is changed. Robustness can be significantly improved by using a variety of instruction formats. The work also investigates the use joint-embedding and contrastive training objectives, using the intuition that the final representation of instructions paraphrased using different formats should be similar. However, it finds that these objectives don't help performance, and provides a hypothesis as to why this is the case.

Abstract: Instruction fine-tuning is a widely used technique to specialise pre-trained models for specific tasks, and
improve zero-shot performance. While a body of work has sought to understand the robustness and general-
isation to new tasks, comparatively little has been done to understand how the format and phrasing of inputs
used during training affects performance. We use the MAVEN-ERE dataset, and train FLAN-T5-Large on a
training set where every example has been paraphrased using twenty different formats. We then evaluate the
impact on performance using an evaluation set where the examples are augmented using unseen instruction
formats, as well as the consistency of the model answers and representations across the unseen formats. We
find that only using one instruction format during training leads to a model which is not robust to other
instruction formats. By training on a range of instruction formats, we are able to significantly improve the
performance and consistency of the model. However our paraphrase-trained model, while more robust in
general, can still experience sudden and sharp changes in performance from minor changes to the format. We
also investigate the impact of using different training objectives which encourage consistent representations
between paraphrases. However, we find there is little correlation between the consistency of the model’s final
vector representation of paraphrased inputs in embedding space, and the answer consistency. We present a
hypothesis as to why this might be the case. This work emphasises the importance of training on a wide
variety of instruction formats when fine-tuning models.
