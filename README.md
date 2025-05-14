# HoomanMLTK

**HoomanMLTK** is a personal machine learning toolkit that provides modular, reusable components for a variety of ML workflows.  
This project is designed to centralize helpful utilities and abstractions developed during experimentation, prototyping, or production-level ML work.

---

## Modules

| **Domain** | **Tool / Class**     | **Description** |
|------------|----------------------|-----------------|
| `nlp`      | `TextPreprocessor`   | A flexible and efficient transformer for cleaning tasks including URL removal, contraction expansion, punctuation removal, spell checking, stemming, lemmatization, and more. Supports parallel processing for faster transformations on large datasets. |

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
