# Texts

This collection of texts contains 324 Wikipedia articles, which are linked to the German-language Zwinger, Dresden article.
These texts cover parts of the Zwinger complex, important personalities connected to the Zwinger as well as articles about the Baroque or specific architectural elements.
In addition, we include two scientific publications about the Zwinger in order to test our methodology on longer, more complex texts.

Each annotated text is a set of three files:

- a plain text file containing the article `.txt`
- a JSON file containing a list of all the annotations in the text `.json`
- a BibTex file containing metadata about the text `.bib`

The JSON is structured as follows:
Each annotation is located by `start` and `end` position in the plain text.
`found_term` represents the word at this position.
Each assigned label in `labels` consists of the `search_term`, its IDs in the vocabularies (`wd_id` &rarr; Wikidata, `aat_id` &rarr; Getty Art & Architecture Thesaurus (AAT)) as well as the `confidence`, i.e., the similarity score with respect to the found term.

```json
[
  {
    "start": 15146,
    "end": 15152,
    "found_term": "Gesims",
    "labels": [
      {
        "aat_id": 300002944,
        "wd_id": "Q35473",
        "search_term": "Fenster",
        "confidence": 0.6477
      },
      {
        "wd_id": "Q747567",
        "search_term": "Risalit",
        "confidence": 0.7793
      },
      {
        "aat_id": 300002526,
        "wd_id": "Q183061",
        "search_term": "Fassade",
        "confidence": 0.7063
      },
      {
        "aat_id": 300001788,
        "wd_id": "Q328092",
        "search_term": "Gesims",
        "confidence": 1.0
      },
      {
        "aat_id": 300002737,
        "wd_id": "Q175112",
        "search_term": "Pilaster",
        "confidence": 0.86
      }
    ]
  },
  ...
]
```

Example of a BibTex file:

```bibtex
@misc{wiki:Dresdner_Barock,
    title = "Dresdner Barock--- {W}ikipedia{,} The Free Encyclopedia",
    year = "2023",
    url = "https://de.wikipedia.org/wiki/Dresdner_Barock",
    note = "[Online; accessed 20-March-23]"
}
```