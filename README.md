# 🧠 Image Caption Generator using VGG16 + LSTM

Generate human-like captions for images using deep learning. This project combines **Convolutional Neural Networks (CNNs)** for image feature extraction and **Recurrent Neural Networks (RNNs)** for natural language generation, trained on the **Flickr8k** dataset.

---

## 📌 Project Summary

This project aims to automatically generate descriptive captions for images by learning the mapping between visual features and text sequences. It uses a **pretrained VGG16 model** for image feature extraction and an **LSTM-based decoder** to generate captions word by word.

---

## 🧠 Model Architecture

- **Encoder**: VGG16 (pretrained on ImageNet; FC layers removed)
- **Decoder**: LSTM with word embedding, fully connected, and softmax layers
- **Tokenizer**: Trained on the Flickr8k caption corpus
- **Loss Function**: Categorical Crossentropy
- **Optimizer**: Adam

---

## 📊 Results

| Metric   | Score  |
|----------|--------|
| BLEU-1   | 0.53   |
| BLEU-2   | 0.31   |

- BLEU scores are used to evaluate the closeness of generated captions to human-written ones.
- Results were improved by using **VGG16** and minimal caption preprocessing.

---

## 🗃️ Dataset

- **Flickr8k** dataset: 8,000 images with 5 captions each
- Data is processed in **batch mode**
- Captions cleaned and tokenized for model training

---

## 🔍 Key Observations

- **BLEU scores plateaued** without data augmentation or advanced tuning
- **Pretrained VGG16** model helped improve feature representation and overall accuracy
- Dataset size limits generalization; using larger datasets like Flickr30k or MS COCO could further improve performance

---

## 📚 References

- [Flickr8k Dataset](https://github.com/jbrownlee/Datasets)
- [VGGNet (Simonyan & Zisserman, 2014)](https://arxiv.org/abs/1409.1556)
- [BLEU Score – Wikipedia](https://en.wikipedia.org/wiki/BLEU)
