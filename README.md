# genderbias_instruction_tuning

Here we present a method to quantify stereotype congruence in instruction input- output tasks and we implement a preliminary pipeline to investigate the propogation of gender bias in instruction-tuned systems that use LLM generated instances for finetuning.

# Pipeline

1. generate_instances.ipynb

    Prompt GPT-3.5 with prompts in data to generate new instruction-output instances 

2. analyze_effect_size.ipynb

    Compute the WeFAT effect size for all generated instances

3. prep_data_and_finetune_gpt.ipynb

    Splits data into female associated, male associated, and neutral using WeFAT scores
    Finetunes 3 GPT-3.5 models using these datasets

4. analyze_stereotype_congruence.ipynb
    Computes the number of stereotype incongruent instances there are in each dataset

# Data

Found in /data folder - includes GPT input-output instances and WeFAT scores
