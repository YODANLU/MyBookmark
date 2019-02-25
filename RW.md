Three main sub-tasks in SLU are domain and intent detection, and slot filling. Generally, the domain and intent detection are treated as a classification task, and the slot filling as a sequence labeling task.  In statistical approaches, traditional models for the domain and intent detection include support vector machine and maximum entropy. For the slot filling, sequence models can be applied such as maximum entropy Markov models and conditional random fields. Recently, deep learning models such as recurrent neural networks (RNNs) and convolutional neural networks (CNNs) have been explored in SLU. In addition, many joint models have been proposed to use the relationships between three sub-tasks. The joint models with attention mechanism and the slot-gated mechanism achieved the state-of-the-art performance.
More recently, the BERT which stands for Bidirectional Encoder Representations from Transformers was introduced. Pre-train BERT representations can be fine-tuned with additional output layers. The BERT model achieved state-of-art results on a wide range of tasks including classification and sequence labeling tasks for language understanding. So, the BERT model would be effective in SLU tasks even though not many studies have been published yet. Our model is also based on the BERT model. However, we used a small and simplified model with because of limited computational resource in on-device environment.
The joint online SLU model was proposed. Instead of performing SLU tasks at the end of the speech, the model can produce real time results for intent detection and slot filling while speaking. It matches most speech recognizers that support online decoding. However, the RNN-based online model requires a large amount of re-calculation when the first word changes in the intermediate speech recognition results. Our proposed model alleviates this problem by using the Transformer based model that has a weak dependency on previous calculations.
Various methods have been proposed to increase the efficiency of deep neural networks: Knowledge distillation, low-rank decomposition, network quantization and weight pruning. Although we did not focus on these methods in this paper, we plan to apply these methods to our on-device deep neural network models.
3	Proposed Approach
Given x
YS1….
 
[ REF ] 
https://arxiv.org/pdf/1811.02454.pdf 
https://arxiv.org/pdf/1801.05149.pdf
https://www.ijcai.org/Proceedings/16/Papers/425.pdf
http://www.aclweb.org/anthology/N18-2118
https://arxiv.org/pdf/1609.01462.pdf
https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6289058
