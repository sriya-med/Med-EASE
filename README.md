# Med-EASE

# medical-diagnosis-simplifier
NLP project for simplifying medical diagnoses using the Med-EASi dataset.

## Getting Started Instructions

1. Clone Repository: 

`git clone ___`<br>
`cd Med-EASE`

1. Create venv and activate:

`python -m venv venv`
`source venv/bin/activate`

4. Upgrade Pip and install packages from requirements.txt

`pip install -r requirements.txt`

5. When you install new package, remember to update requirements.txt and commit it.

`pip freeze > requirements.txt`



## File Directory:

- `notebooks/ `: testing out (use vs code colab extension) <br>
    - `flan_t5_base_model.ipynb`:   --> used flan-t5-base model to fine tune Med-EASi dataset on and evaluate with SARI< ROUGE, and BLEU<br>

- `models/` : saved model output csv files<br>
