# Generative AI and Machine Learning for Crime Prediction

Research code and data accompanying a peer-reviewed article comparing **Machine Learning** and **Generative AI** for crime-suspect prediction using public Toronto Police data.

---

## Abstract

This repository supports a research article (currently under peer review as of June 2025) that compares how traditional ML (e.g. Gradient Boosting, XGBoost) and Generative AI perform on a specific crime-suspect prediction task. The dataset is derived from open Toronto Police Service records. See the **pre-print** and the notebook for methodology and results.

---

## Repository contents

| Item | Description |
|------|-------------|
| `crime_prediction.ipynb` | Main notebook: data loading, ML pipeline, and visualisation |
| `training_set_200_entries.csv` | Sample training data (representative subset of 2021 arrests) |
| `RBDC-ARR-TBL-001.csv` | Toronto Police “Arrests and Strip Searches” source data |
| `2021_data.csv` | 2021 arrest data used for evaluation |
| `*_Prediction_Accuracy.csv` | Accuracy metrics for XGBoost and LLM predictions |
| `predicted_2021_*.csv` | Model predictions (XGBoost and LLM) |

**Note:** The notebook expects `training_set.csv` and `empty_race_field_2021_ML.csv` as inputs. These can be created from the included CSVs (e.g. from `RBDC-ARR-TBL-001.csv` or `2021_data.csv`) following the methodology described in the notebook and the paper.

---

## Data source

Arrest and strip-search data are from the **Toronto Police Service** open data portal:

- [Arrests and Strip Searches (RBDC-ARR-TBL-001)](https://data.torontopolice.on.ca/datasets/TorontoPS::arrests-and-strip-searches-rbdc-arr-tbl-001/about)

Use of this data is subject to the Toronto Police Service open data terms of use.

---

## Setup and usage

### Requirements

- Python 3.8+
- Dependencies: `pandas`, `scikit-learn`, `xgboost`

### Installation

```bash
git clone https://github.com/snsn3/Gen_AI_Crime_Prediction_Research_Article.git
cd Gen_AI_Crime_Prediction_Research_Article
pip install -r requirements.txt
```

### Running the analysis

1. Prepare the inputs expected by the notebook (`training_set.csv`, `empty_race_field_2021_ML.csv`) from the provided CSVs if needed.
2. Open `crime_prediction.ipynb` in Jupyter or [Google Colab](https://colab.research.google.com/github/snsn3/Gen_AI_Crime_Prediction_Research_Article/blob/main/crime_prediction.ipynb).
3. Run all cells to reproduce the ML pipeline and visualisations.

---

## Publication and citation

- **Pre-print (SSRN):** [https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5118289](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5118289)  
  The article is under peer review; please cite the pre-print when referring to the methodology or results.

- **Citing this repository:** A `CITATION.cff` file is included. You can use it with tools that support [Citation File Format](https://citation-file-format.github.io/), or cite the repository URL and the SSRN pre-print.

- **Published article:** [Journal of Responsible Technology - Elsevier ](https://doi.org/10.1016/j.jrt.2026.100160)

---

## License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## Funding and acknowledgments

This research is supported by Canada’s **Social Sciences and Humanities Research Council (SSHRC)** through the [Canada Vanier Graduate Scholarships](https://vanier.gc.ca/en/home-accueil.html).
