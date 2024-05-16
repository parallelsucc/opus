## Arxiv link: https://arxiv.org/abs/2405.08570
## opus
## Reproducible Code：https://github.com/parallelsucc/opus/tree/reproduction

This article explores the adaptive relationship between Encoder Layers and Decoder Layers using the SOTA model Helsinki-NLP/opus-mt-de-en, which translates German to English. The specific method involves introducing a bias-free fully connected layer between the Encoder and Decoder, with different initializations of the layer's weights, and observing the outcomes of fine-tuning versus retraining. Four experiments were conducted in total. 

-	Using original pre-trained model weights and initializing the fully connected layer weights to maintain the original connections, where each Decoder Layer's input is from the 6th Encoder Layer. Through fine-tuning, these weights adapt towards optimal configurations.
-	Fine-tuning the original pre-trained model as a baseline experiment.
-	Initializing the fully connected layer weights with Granularity Consistent Attention.
-	Initializing all layer weights with a variance of 0 and mean of 1, with the fully connected layer between Encoder and Decoder initialized to maintain original connections.

The results suggest that directly modifying the pre-trained model structure for fine-tuning yields suboptimal performance. However, upon observing the outcomes of the experiments with retraining, this structural adjustment shows significant potential.


