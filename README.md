# Automatic Image Captioning with Deep Learning

## Introduction
Google's Conceptual Captions dataset provided a new challenge in image captioning, prompting advancements in AI-driven education. Generating descriptive captions automatically from images is crucial for extracting meaningful information.

This project aims to develop a Deep Learning application that merges cutting-edge techniques in computer vision and natural language processing. The system takes images as inputs and generates human-readable descriptions.

## Objective
The main goal is to create a useful application that leverages both computer vision and natural language processing to generate accurate and understandable captions solely from images.

Understanding various techniques to train Neural Networks faster through the use of optimizers is another objective.

## Data Overview
Utilizing the flickr8k dataset, which consists of over eight thousand images and their corresponding captions, forms the foundation of this project.

When observing the provided images:

- Left image: "beige puppy walks across the floor"
- Middle image: "blond girl in brown shirt with black pen up her nose"
- Right image: "little girl smiles as she wears white bowl on the top of her head"

## Model Structure
The image captioning task involves two models:

- Image Based Model: Extracts features from an image.
- Language Based Model: Generates a sentence about the picture using previous captions and features from the image-based model.

### Image Based Model – Convolutional Neural Network (CNN)
Transfer learning with the pre-trained VGG16 model is utilized to extract image features.

### Language Based Model – Recurrent Neural Network (RNN)
Caption sequences are generated using word embedding and LSTM layers.

## Data Engineering
Cleaning functions for existing captions were created, reducing the vocabulary size and generating a word cloud for common phrases.

## Image Based Model - CNN
Features for each image are created using VGG16's pre-trained networks. PCA visualization is used to understand the distribution of features.

## Language Based Model – RNN
An unfolded RNN network is employed to predict the next word in a sequence.

## Optimizers for Faster Training
Various optimizers such as Gradient Descent, Gradient Descent with Momentum, RMSProp, and Adam are explored to expedite training.

## Model Result
Adam optimizer outperforms others in terms of loss. Model-generated captions at different epochs are examined to monitor overfitting.

## Model Evaluation
Bilingual Evaluation Understudy (BLEU) is used to evaluate the similarity between model-generated sentences and reference sentences.

## Conclusion
The project successfully builds a system for generating captions from images. Adam optimizer proves effective in training the model. However, the model may still produce incorrect captions, highlighting the need for further improvement.

## Future Work
Future work includes incorporating larger datasets, exploring different transfer layers, generating multiple sequences, and exploring alternative evaluation metrics.

## Reference
- [1] Cyrus Rashtchian, Peter Young, Micah Hodosh, and Julia Hockenmaier. Collecting Image Annotations Using Amazon's Mechanical Turk.
- [2] Recurrent Neural Networks Tutorial
- [3] How to Train Neural Networks Faster with Optimizers
- [4] Kishore Papineni, Salim Roukos, Todd Ward, Wei-Jing Zhu. (2012). BLEU: a Method for Automatic Evaluation of Machine Translation.
- [5] Develop an Image Captioning Deep Learning Model using Flickr 8K data