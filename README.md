# RuQASPER
RuQASPER is reworked version of [QASPER dataset](https://paperswithcode.com/dataset/qasper) translated into Russian. Along with the following is provided: a trained suzume_lora2 model with train scripts, updated LongBench benchmark, tools for building dataset extensions and a web interface for the suzume model.  


## General purpouse of the project
The main goal of RuQASPER is to provide an extencive toolset for NLP focused on academic literature. It aims to solve a problem of accurately retrieving information from long (around 30.000 tokens) research papers via QA and summarization. 

## Original Dataset Simplification and Translation
The original QASPER dataset while being highly detailed provides very complicated structure that makes it difficult to work with it.

We rework the original structure and organize the data in the following way:

* “id” - represents an ID of a research paper in the original dataset;
* “titles” - contains a title of a paper;
* “abstracts” - contains an abstract of a paper;
* “full_texts” - contains original paragraphs of papers concatenated in a singular string;
* “question_id” - represents an ID of a question asked to a research paper;
* “unanswerables” - reflects the possibility of answering a question given information present in a paper;
* “questions” - contains a question to a paper’s content;
* “answers” - contains an answer to a provided question;
* “evidences” - contains evidence accompanying given answers;
* “figures_and_tables” - contains references to figures and tables originally present in a paper;
* “split” - contains information on the split that a dataset entry originated from.

The origianl QASPER dataset is translated into Russian using Google Translate API. 

## The Data
Different versions of the dataset can be found below:

* https://huggingface.co/datasets/Anper3004/CLSumInstruct
* https://huggingface.co/datasets/Anper3004/QasperSumInstruct
* https://huggingface.co/datasets/Anper3004/QasperQAInstruct
* https://huggingface.co/datasets/Anper3004/CLQAInstruct

## Russian Dataset Extensions
RuQASPER provides a pipeline for creating dataset extensions in Russian. The main extenstion that initially comes with the dataset is a set of research papers in lingistics domain initially gathered as a part of [CATS&KITTENS dataset](https://scholarsarchive.byu.edu/rlj/vol71/iss1/7/).

The code for creating custom extensions for the dataset in .csv format is provided in dataset_building folder of this repo. The pdf_to_df.ipynb notebook can be used to initially parse texts in .pdf format. After that, get_qas_gpt.ipynb can be used to generate the QA part of the dataset. The latter is saved as as .csv file and can be merged with the main RuQASPER csv. 

![alt text][img/dataset_extension.png]

## Running Model and Benchmark 
Scripts to run the model and updated LongBench benchmark can be found in longbench.ipynb. It is recommended to launch the script with at least 80 GB VRAM avaliable. A web interface for the model is also provided in qasper_interface.ipynb. Metrics can be evaluated with scores.ipynb. 