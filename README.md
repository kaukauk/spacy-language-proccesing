# spacy-language-proccesing

Short scripts I wrote in 2021 to try out natural language processing with spaCy: part-of-speech tagging, dependency parsing and named-entity recognition, with displaCy visualisations.

## What it does

- `main.py`: parses an example sentence, prints each token's text, part-of-speech tag and dependency label, and saves a dependency-parse diagram as an SVG (an example output is in `sentence_connections.svg`)
- `spacy-tutorial.py`: runs named-entity recognition on a text file and prints each entity with its label, then serves an entity-highlighting view in the browser using `displacy.serve`

## Tech

Python, spaCy (`en_core_web_sm` model), displaCy

## Running it

```bash
pip install spacy ipython
python -m spacy download en_core_web_sm
python main.py
python spacy-tutorial.py
```

## Notes

- `main.py` writes its SVG to `spacy-NLP/sentence_connections.svg`. Create that folder first, or change the output path.
- `spacy-tutorial.py` reads a sample text file (`wiki_us.txt`) from the freeCodeCamp spaCy course materials, using a hard-coded local path. The data folder is not included (it is listed in `.gitignore`), so download it and update the path before running.
- This is a learning project that follows the freeCodeCamp spaCy tutorial and the spaCy documentation examples.
