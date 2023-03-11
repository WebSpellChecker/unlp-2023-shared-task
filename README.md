# RedPenNet
A public repository containing the research work on RedPenNet approach.
Additional materials related to the article "RedPenNet for Grammatical Error Correction: Outputs to Tokens, Attentions to Spans" will appear here over time.

## Synthetic Data
We generated over 3.7 millions Ukrainian data sentences ([Download](https://wsc-files.s3.amazonaws.com/unlp2023_data/synthetic_back_translation_uk.zip))  based on error-free texts taken from data corpora presented on https://lang.org.ua/uk/corpora/ website. Around 800K sentences have at least one generated error. For our error generation approach, we utilized mbart-large-50 as the pretrain model, which we trained using the back translation method (https://aclanthology.org/N18-1057) on the training data from the UA-GEC dataset. Our task was to transduce the error-free input text sequence into the erroneous one. The synthetic data generation model was trained on a Google Colab Premium GPU instance for 8 epochs, with a batch size of 4, a learning rate of 1e-5, and a maximum input and output length of 128 tokens each.
