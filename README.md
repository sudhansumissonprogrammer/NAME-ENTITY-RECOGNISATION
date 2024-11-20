# Named Entity Recognition (NER) with SpaCy

Named Entity Recognition (NER) is a technique in NLP that identifies and classifies named entities in text into predefined categories such as persons, organizations, locations, dates, and more.

## Prerequisites

Ensure you have SpaCy installed and the English language model downloaded. You can install SpaCy using pip:

```bash
pip install spacy
```

Download the English model:

```bash
python -m spacy download en_core_web_sm
```

## Steps for NER using SpaCy

### 1. **Import SpaCy**

Start by importing the SpaCy library and loading the language model.

```python
import spacy

# Load the English language model
nlp = spacy.load("en_core_web_sm")
```

### 2. **Process Text**

Input the text you want to analyze and process it with the SpaCy pipeline.

```python
# Sample text
text = "Apple is looking at buying U.K. startup for $1 billion."

# Process the text
doc = nlp(text)
```

### 3. **Extract Named Entities**

Iterate through the processed document to extract named entities and their labels.

```python
# Extract and print named entities
for ent in doc.ents:
    print(f"Entity: {ent.text}, Label: {ent.label_}")
```

### 4. **Visualizing Named Entities**

SpaCy provides a visualization tool to display the named entities in the text.

```python
from spacy import displacy

# Visualize named entities
displacy.serve(doc, style="ent")
```

## Example Output

When you run the above code, you might see output like:

```
Entity: Apple, Label: ORG
Entity: U.K., Label: GPE
Entity: $1 billion, Label: MONEY
```
---

SpaCy’s [official documentation](https://spacy.io/usage/training#ner)
