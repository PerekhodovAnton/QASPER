---
license: other
library_name: peft
tags:
- llama-factory
- lora
- generated_from_trainer
base_model: /home/asperekhodov/.cache/huggingface/hub/models--lightblue--suzume-llama-3-8B-multilingual/snapshots/a91a26333d22b2382025e4e1f5a7869142a683c3
model-index:
- name: suzume_lora2
  results: []
---

<!-- This model card has been generated automatically according to the information the Trainer had access to. You
should probably proofread and complete it, then remove this comment. -->

# suzume_lora2

This model is a fine-tuned version of [/home/asperekhodov/.cache/huggingface/hub/models--lightblue--suzume-llama-3-8B-multilingual/snapshots/a91a26333d22b2382025e4e1f5a7869142a683c3](https://huggingface.co//home/asperekhodov/.cache/huggingface/hub/models--lightblue--suzume-llama-3-8B-multilingual/snapshots/a91a26333d22b2382025e4e1f5a7869142a683c3) on the QasperQAInstruct, the QasperSumInstruct, the CLSumInstruct and the CLQAInstruct datasets.

## Model description

More information needed

## Intended uses & limitations

More information needed

## Training and evaluation data

More information needed

## Training procedure

### Training hyperparameters

The following hyperparameters were used during training:
- learning_rate: 1e-05
- train_batch_size: 2
- eval_batch_size: 8
- seed: 42
- gradient_accumulation_steps: 4
- total_train_batch_size: 8
- optimizer: Adam with betas=(0.9,0.999) and epsilon=1e-08
- lr_scheduler_type: cosine
- lr_scheduler_warmup_ratio: 0.1
- num_epochs: 1.0
- mixed_precision_training: Native AMP

### Training results



### Framework versions

- PEFT 0.11.1
- Transformers 4.41.1
- Pytorch 2.3.0+cu121
- Datasets 2.19.1
- Tokenizers 0.19.1