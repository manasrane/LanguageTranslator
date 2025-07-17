
# 🌐 Language Translator — Seq2Seq Transformer (PyTorch)

A neural machine translation (NMT) model built completely from scratch using PyTorch. This project implements the original Transformer architecture for sequence-to-sequence learning, without relying on high-level frameworks like Hugging Face or Fairseq.

> **Reference**: Inspired by [hkproj/pytorch-transformer](https://github.com/hkproj/pytorch-transformer) — shoutout to the creator! His work was instrumental in helping me understand how Transformers work. You can also check out his [YouTube channel](https://www.youtube.com/watch?v=ISNdQcPhsts) for great deep learning content.



## 🚀 Features

* Full encoder–decoder Transformer architecture
* Manual implementation of:

  * Positional encoding
  * Scaled dot-product attention
  * Multi-head attention
  * Masking (causal and padding)
* SOS/EOS/PAD token handling
* Greedy decoding for inference
* Training loop with validation and checkpointing
* Preprocessing pipeline using Hugging Face `tokenizers` and `datasets`
* Runs on CPU (with optional GPU acceleration via `torch.cuda`)

---

## 📊 Model Architecture

```
Input Sentence (Source) --> Tokenizer --> Encoder -->
                                               ⬇
                                  Transformer Model
                                               ⬆
Target Sentence (Shifted Right) --> Tokenizer --> Decoder -->
                                               ⬇
                                      Output Tokens
```

---

## 📁 Project Structure

```
language-translator/
├── train.py                 # Training loop
├── model.py                 # Transformer model architecture
├── dataset.py               # Custom Dataset class
├── utils.py                 # Utility functions
├── config.json              # Hyperparameter settings
├── checkpoints/             # Saved model checkpoints
└── README.md                # Project documentation
```

---

## 📦 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/language-translator-transformer.git
cd language-translator-transformer
```

### 2. Create and Activate a Virtual Environment

```bash
python3 -m venv mlenv
source mlenv/bin/activate  # On Windows: mlenv\Scripts\activate
pip install -r requirements.txt
```

### 3. Run the Training Script

```bash
python train.py
```

> 💡 Currently set to use CPU by default. GPU training (e.g., NVIDIA CUDA) can be enabled by modifying the device configuration in `train.py`.

---

## 🧪 Sample Output

```
SRC:  Hello, how are you?
TGT:  Bonjour, comment ça va ?
PRED: Bonjour, comment vas-tu ?
```

---

## 🧠 Lessons Learned

* Implemented core Transformer modules from scratch
* Understood tokenization, padding, and attention masks
* Built end-to-end data loading, batching, and checkpointing logic
* Debugged training on CPU without third-party abstractions
* Explored practical training limitations and optimization strategies

---

## ⚡ Future Work

* [ ] Add BLEU score evaluation
* [ ] Implement beam search decoding
* [ ] Integrate Intel OpenVINO for Arc GPU acceleration
* [ ] Scale to larger corpora like WMT
* [ ] Create a Streamlit or Flask-based demo app

---

## 📜 References

* [Attention Is All You Need (Vaswani et al.)](https://arxiv.org/abs/1706.03762)
* [The Annotated Transformer](http://nlp.seas.harvard.edu/2018/04/03/attention.html)
* [Hugging Face Datasets](https://huggingface.co/docs/datasets)

---

## 📄 License

MIT License

---

Let me know if you'd like a badge section (like `Build Status`, `License`, etc.) or want to add visual examples (plots, attention weights, etc.)!
