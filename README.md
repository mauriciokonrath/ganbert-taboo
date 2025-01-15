# ganbert-taboo
GAN-BERT implementation in PyTorch, adapted for the Monsanto dataset. Utilizes Generative Adversarial Networks to enhance text classification with limited labeled data. 

# GAN-BERT (PyTorch and HuggingFace Compatible)

This repository provides an implementation of the GAN-BERT model in PyTorch, adapted for the Monsanto dataset. GAN-BERT leverages a Generative Adversarial Network (GAN) framework to enable effective semi-supervised learning, making it robust for scenarios with limited labeled data. The implementation is compatible with HuggingFace and supports architectures beyond BERT, such as RoBERTa and ALBERT.

## About GAN-BERT

GAN-BERT is an extension of the BERT model that introduces a GAN-based Discriminator-Generator architecture:

- **Generator (G):** Produces "fake" vector representations of sentences.
- **Discriminator (D):** Classifies sentences into task categories (k categories) or recognizes fake examples (k+1 category).

The semi-supervised learning schema allows the model to train on both labeled and unlabeled data, improving performance on tasks with scarce annotated material. 

## Key Features

- **Flexibility:** Works with various architectures (BERT, RoBERTa, ALBERT, etc.).
- **Enhanced Learning:** Trains effectively with a minimal labeled dataset and a large unlabeled corpus.
- **Adapted Dataset:** This version is tailored for the Monsanto dataset, specifically designed for text classification tasks.

## Dataset

The Monsanto dataset replaces the original TREC dataset and includes:

1. **Labeled Monsanto Data:** Adapted with relevant categories.
2. **Unlabeled Monsanto Data:** Provides a robust corpus for semi-supervised learning.
3. **Test Data:** Evaluates the model's performance.

## Getting Started

### Installation

Clone this repository and install the required dependencies:

```bash
git clone <repository-url>

pip install -r requirements.txt"

sh run_experiment.sh
```

## References

- Croce, Danilo, Castellucci, Giuseppe, and Basili, Roberto. 2020. *GAN-BERT: Generative Adversarial Learning for Robust Text Classification with a Bunch of Labeled Examples*. Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics, pages 2114–2119. Online. Association for Computational Linguistics. [Link](https://www.aclweb.org/anthology/2020.acl-main.191)
- Ian Goodfellow, Jean Pouget-Abadie, Mehdi Mirza, Bing Xu, David Warde-Farley, Sherjil Ozair, Aaron Courville, and Yoshua Bengio. 2014. *Generative Adversarial Nets*. Advances in Neural Information Processing Systems 27, pages 2672–2680. Curran Associates, Inc.
- Tim Salimans, Ian Goodfellow, Wojciech Zaremba, Vicki Cheung, Alec Radford, Xi Chen, and Xi Chen. 2016. *Improved Techniques for Training GANs*. Advances in Neural Information Processing Systems 29, pages 2234–2242. Curran Associates, Inc.
  
