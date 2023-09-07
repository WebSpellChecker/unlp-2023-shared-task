# Grammatical Error Correction (GEC) for Ukrainian: Shared Task Repository
Welcome to the collaborative repository presenting the WebSpellChecker team's approach towards Grammatical Error Correction (GEC) for the Ukrainian language. You can learn more about our methodology in the article ["RedPenNet for Grammatical Error Correction: Outputs to Tokens, Attentions to Spans"](https://aclanthology.org/2023.unlp-1.15/). This repository will periodically be updated with new public data.

## Synthetic data
We are excited to share a substantial dataset containing over 3.7 million synthetic Ukrainian sentences, which you can download [here](https://wsc-files.s3.amazonaws.com/unlp2023_data/synthetic_back_translation_uk.zip). The dataset is built upon error-free texts sourced from data corpora presented on the [lang-uk website](https://lang.org.ua/en/corpora/).

## Generation methodology
In this endeavor, we generated sentences utilizing the `mbart-large-50` as the pretrained model. This model was fine-tuned using a [backtranslation method](https://aclanthology.org/N18-1057) on training data extracted from the [UA-GEC dataset](https://github.com/grammarly/ua-gec). This process enabled us to transduce error-free input text sequences into sequences containing synthetic errors. Notably, approximately 800K sentences in this dataset contain at least one generated error. Our model training process took place over 8 epochs on a Google Colab Premium GPU instance. We used a batch size of 4 and a learning rate of 1e-5, limiting input and output lengths to a maximum of 128 tokens each.

## License
The synthetic data available through this repository is generated based on texts from the `lang-uk` corpora and retains the same license — [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/). We encourage users to familiarize themselves with the license terms before utilizing the data. By accessing and using the synthetic data, you agree to abide by the stipulated license terms, promoting ethical use and collaboration within the research community.
