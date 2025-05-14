# HoomanMLTK

**HoomanMLTK** (Machine Learning ToolKit) is a personal machine learning toolkit that provides modular, reusable components for a variety of ML workflows.  
This project is designed to centralize helpful utilities and abstractions developed during experimentation, prototyping, or production-level ML work.

---

## Modules

| **Domain** | **Tool / Class**     | **Description** |
|------------|----------------------|-----------------|
| `nlp`      | `TextPreprocessor`    | A flexible and efficient transformer for cleaning and preprocessing text data, built on top of **NLTK**, **TextBlob**, **re**, and **contractions**. It supports a wide range of text transformation tasks, including: <br> - **URL Removal**: Removes URLs to clean up the text. <br> - **Contraction Expansion**: Expands common contractions (e.g., "don't" → "do not"). <br> - **Punctuation Removal**: Strips punctuation to reduce noise. <br> - **Spell Checking**: Corrects spelling errors with **TextBlob**. <br> - **Stemming & Lemmatization**: Reduces words to their base forms using **NLTK**'s stemmers and lemmatizers. <br> - **Parallel Processing**: Accelerates text transformations on large datasets. <br> - **Customizable Options**: Apply only the transformations you need. <br> - **Flexible Output**: Return preprocessed text as a string or a list of tokens. |

---

## Installation

Install the package from [PyPI](https://pypi.org/project/hoomanmltk/) via:

```bash
pip install hoomanmltk
````

Or install directly from GitHub (for latest changes):

```bash
pip install git+https://github.com/hoom4n/HoomanMLTK.git
```

---

## Quick Start

```python
from hoomanmltk.nlp import TextPreprocessor

texts = ["if i ever were to lose you" , "Take me on" , "Take on me"]

processor = TextPreprocessor(
    url_remove=True,
    expand_contractions=True,
    remove_punctuation=True,
    lemmatize=True,
    output_mode="text"
)

cleaned = processor.fit_transform(texts)
print(cleaned)
```


---

## License

This project is licensed under the **MIT License**.
See the [LICENSE](LICENSE) file for more details.



## Links

* [PyPI Project](https://pypi.org/project/hoomanmltk/)
* [GitHub Repository](https://github.com/hoom4n/HoomanMLTK)
