# Med-EASE

# medical-diagnosis-simplifier
NLP project for simplifying medical diagnoses using the Med-EASi dataset.

## Getting Started Instructions

1. Clone Repository: 

`git clone https://github.com/sriya-med/Med-EASE.git`<br>
`cd Med-EASE`

1. Create venv and activate:

`python -m venv venv`
`source venv/bin/activate`

4. Upgrade Pip and install packages from requirements.txt (only necessary if you run code locally)

`pip install -r requirements.txt`

## Running the code:
- Our code is written as jupyter notebooks. All files require significant compute power. In order to run these files, we used Google Colab with the free Student Pro account. IMPORTANT: Download the VS Code Google Colab Extension, connect to T4 GPU and run the notebook cells. 



## File Directory:

- `notebooks/ `: testing out (use vs code colab extension) <br>
    - `flan_t5_base_model.ipynb`:   --> used flan-t5-base model to fine tune Med-EASi dataset on and evaluate with SARI< ROUGE, and BLEU<br>
    - `rl_learning.ipynb`:   --> used flan-t5-base model with parameters from `flan_t5_base_model.ipynb` to create reward function to get optimized output<br>
    - `singlerun_flan_T5_base_model.ipynb`:   --> experimental code to predict on a single example (baseline) <br>
    - `flanT5Tuned_GPT-Neo_UnslothLlama_Models.ipynb`:   --> This notebook tests 3 different models for the output: The Flan-T5 Instruction Tuned Model, the GPT-Neo-125m Model, and the Unsloth Llama 3.1-8B Instruct Model. The Flan-T5 Instruction Tuned model takes the base model and adds input prompts and the training arguments are fine-tuned to display the metric results (You will need to paste an API Key from wandb to run this portion of the notebook). Used another publicly available model, the GPT-Neo-125m, to fine-tune and compare the results with the respective models. Used the Unsloth Llama 3.1-8B Instruct Model as it had knowledge in the medical field and fine-tuned the model to display and compare the results with the other respective models.<br>
    - `testrun_examples_rl_learning_flan_t5.ipynb`:   --> experimental code to predict on a single example (RL)<br>
    - `llama_model_train.ipynb`:   -->  fine-tunes Llama-3.1-8B-Instruct and saves model to hugging face (if you run this code, you must request gated access to Llama-3.1-8B-Instruct and create access token with read access, and if you want to save model to your profile in hugging face, make sure to rename repo_id and use acccess token with permission to create repo)<br>
    - `llama_model_inference.ipynb`:   --> loads model from where it was saved in a repo on hugging face and predicts on a single example, evaluates metrics on med-easi test dataset<br>




- `model_output/` : saved model output csv files<br>
    -
