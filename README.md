# AngoBERTa Model Card

## 🌐 Introduction

Welcome to AngoBERTa, a masked language model finetuned using multilingual adaptive finetuning. This model has been trained to understand and generate text in various languages, with a focus on Kimbundu, Umbundu, Chokwe, Kikong, and Lua.

## 🤖 Model Details

- **Model Name:** AngoBERTa
- **Repository:** [![Hugging Face](https://img.shields.io/badge/Hugging%20Face-Transformers-orange)](https://huggingface.co/cx-olquinjica/AngoBERTa)

## 📊 Finetuning Details

- **Epochs:** 3.0
- **Training Loss:** 1.5986742023225826
- **Evaluation Loss:** 1.1864104270935059
- **Perplexity:** 3.2753031414994718

## 📈 Evaluation Metrics

- **Evaluation Runtime:** 69.8611 seconds
- **Evaluation Samples:** 2079
- **Samples per Second:** 29.759
- **Steps per Second:** 1.861

## 🚀 Training Details

- **Training Runtime:** 35954.3459 seconds
- **Training Samples:** 206438
- **Samples per Second:** 17.225
- **Steps per Second:** 0.861

## 💻 How to Use AngoBERTa

1. **Install Transformers Library:**
   ```bash
   pip install transformers

## Load the model
 ```python

from transformers import AutoModelForMaskedLM, AutoTokenizer

model_name = "cx-olquinjica/AngoBERTa"
tokenizer = AutoTokenizer.from_pretrained(model_name)
model = AutoModelForMaskedLM.from_pretrained(model_name)
```

## Generate Text
 ```python

input_text = "In Kimbundu, the word for 'hello' is [MASK]."
inputs = tokenizer(input_text, return_tensors="pt")
outputs = model(**inputs)
logits = outputs.logits
```

## Explore Multilingual Capabilities:

AngoBERTa is designed to handle multiple languages, including Kimbundu, Umbundu, Chokwe, Kikong, and Lua. Experiment with various texts in these languages to leverage the model's capabilities.

🙌 Acknowledgments

AngoBERTa is made possible by the Hugging Face Transformers library and the community contributions to pre-trained models.

🐞 Issues and Contributions

If you encounter any issues or have suggestions for improvements, please open an issue on the Hugging Face repository. Contributions are welcome!

📄 License

This model is licensed under the Apache 2.0 license. See the LICENSE file for more details.

Enjoy using AngoBERTa for your multilingual natural language processing tasks! 🌍✨
