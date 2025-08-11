### litsense-wrapper

Python wrapper for the NCBI LitSense2 API. LitSense2 (an update of LitSense) is a NCBI/NLM system for sentence- and paragraph-level semantic search across PubMed abstracts and the PMC Open Access subset, returning the most relevant sentences or passages for a query. It is useful for rapid evidence attribution, biocuration, and comparing new findings with existing literature. Learn more on the [NCBI LitSense2 page](https://www.ncbi.nlm.nih.gov/research/litsense2/).

#### Installation

```bash
pip install litsense-wrapper
```

#### Usage

```python
from litsense_wrapper import LitSense_API

engine = LitSense_API()
results = engine.retrieve(query_str='COVID-19 mechanism', limit=2)

for result in results:
    print(result.text)
```

#### Notes
- Modes supported: `passages` (default) and `sentences`.
- Optional `min_score` to filters results based on similarity scores

