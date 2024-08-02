T5 Fine-Tuning for Question Answering
This project demonstrates how to fine-tune a T5 model on various QA datasets: SQuAD, HotpotQA, and Natural Questions. The fine-tuning process is sequential, and the best model is saved based on the ROUGE-1 F1 score.

Table of Contents
Installation
Usage
Code Overview
Model Saving and Evaluation
Results
Contributing
License
Installation
Prerequisites
Python 3.8+
PyTorch
Transformers library from Hugging Face
Datasets library from Hugging Face
tqdm
pandas
Installation Steps
Clone the repository:

bash
Copy code
git clone https://github.com/your-repo/t5-finetuning.git
cd t5-finetuning
Create a virtual environment:

bash
Copy code
python3 -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
Install the required packages:

bash
Copy code
pip install -r requirements.txt
Usage
To fine-tune the T5 model on the specified datasets, simply run the main script:

bash
Copy code
python main.py
This will sequentially fine-tune the model on SQuAD, HotpotQA, and Natural Questions datasets and save the best models based on the ROUGE-1 F1 score.

Code Overview
The main script performs the following steps:

Initializes the tokenizer and model.
Defines a preprocessing function for the datasets.
Implements a custom callback to save the best model based on the ROUGE-1 F1 score.
Fine-tunes the model sequentially on SQuAD, HotpotQA, and Natural Questions datasets.
Saves the fine-tuned model and tokenizer.
Model Saving and Evaluation
The best model is saved during training based on the ROUGE-1 F1 score. The evaluation results are logged after each epoch, and if there is no improvement for a specified number of epochs, the training is terminated early.

Results
After running the script, the fine-tuned models will be saved in their respective directories:

./t5_squad_finetuned
./t5_hotpotqa_finetuned
./t5_nq_finetuned
Contributing
Contributions are welcome! Please feel free to submit a Pull Request.
