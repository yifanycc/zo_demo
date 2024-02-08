
# Demo for Zeroth-order fine-tuning of Large Language Models


## Run this code

1. Install the required environment
- An conda environment file is stored in the root folder named **'environment.yml'. Create conda environment with 
this file**
- The project is written mainly with python 3.7, torch 2.1.2 and the hugging-face transformers 4.28.1
- Set the CUDA_VISIBLE_DEVICES in CUDA_VISIBLE_DEVICES at 'run_all_large_exp.sh'. (Most test can be fitted within a 40G GPU, except the Adam full model fine-tuning, which need about 80G memory)
- Change the path on top of the 'run_all_large_exp.sh' and the run.py file
2. Experiments available and tested in this code **(run all experiments in 'run_all_albert_fine_tune.sh')**:
- Fine-tuning Llama-2-7B model for SST-2 task with Adam full model fine-tuning
- Fine-tuning Llama-2-7B model for SST-2 task with ZO full model fine-tuning
- Fine-tuning Llama-2-7B model for SST-2 task with Adam LoRA fine-tuning
- Fine-tuning Llama-2-7B model for SST-2 task with ZO LoRA fine-tuning **(We recomment this one for ZO training)**

3. Parameter and Experiments settings
- Most important settings are changed in the shell file (run_all_large_exp.sh/mezo.sh/finetune.sh)
- The code only contains the experiment over Llama-2 models and LoRA/ft setup
- **The experiment use a low-data resource setting, which only pick up 1000 training samples from the dataset**


The code is built base on the github repository of paper 'MeZO: Fine-Tuning Language Models with Just Forward Passes'

We have further implementation over the Bert model and other Parameter-efficient methods (like prefix/adapters/ia3...)

For more question, feel free to contact 'yifanyang@ucsb.edu'

