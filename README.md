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
    - `rl_learning.ipynb`:   --> used flan-t5-base model with parameters from `flan_t5_base_model.ipynb` to create reward function to get optimized output<br>
    - `singlerun_flan_T5_base_model.ipynb`:   --> experimental code to predict on a single example (baseline) <br>
    - `testrun_examples_rl_learning_flan_t5.ipynb`:   --> experimental code to predict on a single example (RL)<br>
    - `llama_model_train.ipynb`:   -->  fine-tunes Llama-3.1-8B-Instruct and saves model to hugging face (if you run this code, you must request gated access to Llama-3.1-8B-Instruct and create access token with read access, and if you want to save model to your profile in hugging face, make sure to rename repo_id and use acccess token with permission to create repo)<br>
    - `llama_model_inference.ipynb`:   --> loads model from where it was saved in a repo on hugging face and predicts on a single example, evaluates metrics on med-easi test dataset<br>




- `model_output/` : saved model output csv files<br>
    -
