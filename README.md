# Domain Specific Knowledge For Large Language Models

## Brief

This is the code repository for the Imperial MEng Computing Individual Project on the above subject title. The project aim is to develop a language model for answering questions on a particular domain, with motivation to uncover the most impactful transferable techniques for doing so. Specifically, this project focuses on the knowledge aspect of such models. The Anatomy domain is used as case study. Initial experiments used Google's Flan T5 base model, and later experiments used Meta's Llama 3 8B model.

## /books

- This folder contains a series of Anatomy text books that were used to create a knowledge base during the RAG experimentation phase of this project.
- anatomybook.pdf - Netter's Clinical Anatomy, John T. Hansen (2019): https://books.google.co.uk/books/about/Netter_s_Clinical_Anatomy.html?id=bqdAtAEACAAJ&redir_esc=y
- anatomybook2.pdf - Human Anatomy and Physiology, Nega Assefa, Yosief Tsige (2003): https://www.cartercenter.org/resources/pdfs/health/ephti/library/lecture_notes/nursing_students/ln_human_anat_final.pdf
- anatomybook3.pdf - Cunningham's Manual of Practical Anatomy: Upper and lower limbs, Rachel Koshi (2017): https://books.google.co.uk/books/about/Cunningham_s_Manual_of_Practical_Anatomy.html?id=LaLlAQAACAAJ&redir_esc=y
- anatomybook4.pdf - Clinical Anatomy: Applied Anatomy for Students and Junior Doctors, Harold Ellis (2006): https://books.google.co.uk/books/about/Clinical_Anatomy.html?id=SgNVVAAfDgIC&redir_esc=y
- anatomybook5.pdf - Grant's Atlas of Anatomy, A. M. R. Agur, Arthur F. Dalley, John Charles Boileau Grant (2013): https://books.google.co.uk/books/about/Grant_s_Atlas_of_Anatomy.html?id=SmflHHbed4EC&redir_esc=y
- oxfordMedicalDictionary.pdf - Oxford Medical Dictionary, Elizabeth Martin (2003): https://www.amazon.co.uk/Concise-Medical-Dictionary-Paperback-Reference/dp/0198607539

## /finetuning

- finetuning_experiment_1.ipynb - This is a single notebook with modifyable parameters for finetuning with LoRA and was used to produce the results of the LoRA finetuning experiment.

## /flan-t5

- t5_on_CNN_and_Daily_Mail.ipynb - This notebook contains the code used to fine-tune and evaluate the Flan T5 model on the CNN and Daily Mail dataset.
- t5_on_CoQA.ipynb - This notebook contains the code used to fine-tune and evaluate the Flan T5 model on the CoQA dataset.
- t5_on_medmcqa.ipynb - This notebook contains the code used to fine-tune and evaluate the Flan T5 model on the medmcqa dataset.
- t5_on_SQuAD.ipynb - This notebook contains the code used to fine-tune and evaluate the Flan T5 model on the SQuAD dataset.

## /miscelaneous

- llama-3-8b-base-medmcqa-performance.txt - This file contains outputs of Llama 3 8B on a range of questions along with the label answers used to manually inspect the responses to try gain an understanding of what the model is doing, and where it is struggling.

## /providing-word-definitions

- create_word_defs_dictionary.ipynb - This notebook contains the code used to create a dictionary of word definitions for medical terms using GPT-3.5 Turbo.
- harvard_med_dict.json - This is one alternative dictionary used to the synthetically created dictionary with GPT-3.5 Turbo.
- llama_3_8B_med_Providing_Definitions_1.ipynb - This notebook contains the code that provides the word definitions created with GPT-3.5 Turbo to the model to evaluate it's answering ability when augmented with definitions.

## /RAG

- create_rag_kb.ipynb - This notebook contains the code used to create various knowledge bases stored in Pinecone used in the different RAG experiments.
- llama_3_8B_med_n_gram.ipynb - This notebook was used to evaluate the models performance on each dataset split by n-gram answer size.
- llama_3_8B_med_RAG_1.ipynb - This notebook was used to evaluate the models peformance for the RAG 1 experiment in which the MedMCQA dataset knowledge base was used. RAG_2 can use the same notebook but a different knowledgebase.
- RAG-4-advanced.ipynb - This notebook applies various LlamaIndex techniques and evaluates the model on each.
- RAG-4-books.ipynb - This notebook evaluates the models performance when using the Anatomy text books from the /books folder as a knowledge base.
- RAG-4-chunk-size.ipynb - This notebook evaluates the impact of varying the chunck size of the documents in the knowledge base.
- RAG-4-k.ipynb - This notebook evaluates the impact of varying the number of documents retrieved per prompt.

## /second-opinion

- second_opinion.ipynb - This notebook contains the code used to run the second opinion experiment from the project.
