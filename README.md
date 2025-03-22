# Georgian BPE Tokenizer

A high-performance Byte-Pair Encoding (BPE) tokenizer optimized for the Georgian language, trained on a 5GB corpus with **0% unknown tokens** and **100% word coverage**.

## Features
- 🚀 **19k+ tokens/sec** processing speed
- 📚 Trained on 800k+ documents from [RichNachos/georgian-corpus](https://huggingface.co/datasets/RichNachos/georgian-corpus)
- 🔍 Supports subword regularization and punctuation isolation
- 🛠️ Easy integration with Hugging Face and NLP pipelines

## Installation
```bash
pip install tokenizers datasets tqdm
```

## Usage

Load the Tokenizer:

```python
from tokenizers import Tokenizer

tokenizer = Tokenizer.from_file('georgian_tokenizer_800k.json')
```

Tokenize text:

```python
encoded = tokenizer.encode("გამარჯობა, სამყარო!")

print(encoded.tokens)  # ['გამარჯობა', ',', 'სამყარო', '!']
```

## Evaluation Metrics (5GB Test Corpus)

| Metric    | Value |
| -------- | ------- |
| Compression Ratio	  | 5.76  |
| Unknown Tokens | 0.00% |
| Tokenization Speed | 19,141/sec |
| Word Coverage	| 100% |
| Avg Tokens per Word	| 1.40 |

## Acknowledgments

Special thanks to:

 - [RichNachos/georgian-corpus](https://huggingface.co/datasets/RichNachos/georgian-corpus) for providing the training corpus.
 - Hugging Face tokenizers library for the BPE implementation

## Contributing

Pull requests are welcome! For major changes, open an issue first.

## Donations 💻

USDT (TRC20): `TGAReh6f4mLJrCo5kVduYV1pBVgdhknJQi` Help us build Georgian AI infrastructure! Server costs for training larger models:

Your support will fund:
- Larger Georgian LLM training (1B+ parameters)
- Expanded corpus collection
- Public GPU resources for Georgian NLP

