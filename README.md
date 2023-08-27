# English to Hindi Text Translation

## Introduction
The aim of this project was to build an effective English to Hindi text translation system using Deep Learning techniques. The project was executed in three distinct parts, each employing different datasets and models to achieve accurate translation. This report provides a comprehensive overview of the entire project, covering data preprocessing, model architectures, inference methods, evaluation metrics, and the results obtained.

## Dataset
### Part 1 and 2:
For these parts, the project utilized the IIT Bombay English-Hindi corpus, a rich parallel corpus containing 15,55,573 pairs of English and Hindi sentences. This dataset also incorporated monolingual Hindi corpus, curated by the Center for Indian Language Technology, IIT Bombay. Each sentence pair ranged from one to fifty words in length.

### Part 3:
The third part of the project employed the English Hindi Parallel Corpora by Clarin, containing 1,25,573 sentence pairs in English and Hindi. The sentence lengths in this dataset ranged from five to thirty words.

## Data Preprocessing
The data preprocessing phase was common across all three parts of the project. The following steps were applied:

1. Removal of Instances with Missing Values: Data points lacking either English or Hindi sentences were removed to ensure data integrity.

2. Elimination of Misleading Instances: Sentences containing words from one language in the other language's column were filtered out.

3. Removal of Numerical Digits: Instances with numerical digits were excluded, while words represented as numbers in text form were retained.

4. Word Cloud Analysis: Sentence length distribution was visualized using word clouds, and sentences containing words between five and ten were discarded.

5. Word Level Tokenization: Tokenization was performed to convert words into tokenized units.

6. Sequence Conversion and Padding: Tokenized units were converted into sequences and padded to ensure consistent input length.

## Deep Learning NLP Models
### Part 1:
An Encoder-Decoder architecture was implemented for this part. Bidirectional Gated Recurrent Units (GRU) were used along with Multi-head Attention Layers. The entire model was built from scratch using TensorFlow.

### Part 2:
For this section, an Encoder-Decoder architecture based on Transformers was employed. This model, also developed from scratch using TensorFlow, aimed to leverage the powerful self-attention mechanism inherent in Transformers.

### Part 3:
The third part involved fine-tuning a pre-trained Encoder-Decoder model from the Hugging Face library. This approach harnessed the advantages of transfer learning to improve translation performance.

## Inference
For parts 1 and 2, two inference methods were implemented:

1. Greedy Search: A straightforward approach where the most likely word is chosen at each step.

2. Minimum Bayes Risk Decode: A more sophisticated decoding technique aiming to minimize the expected risk associated with translations.

For part 3, the Hugging Face translation/encoder-decoder pipeline was utilized for inference, simplifying the process.

## Evaluation Metric
The primary evaluation metric used for all three parts was the BLEU score. BLEU (Bilingual Evaluation Understudy) assesses the quality of translations by comparing them to reference translations.

## Results and Analysis
### Part 1:
The model exhibited signs of overfitting on the test set but demonstrated the ability to accurately translate numerous words in sentences.

### Part 2:
The model in this section displayed significant overfitting during training, leading to incorrect translations and word repetition. However, the project deepened the understanding of Transformer concepts.

### Part 3:
In this part, overfitting was minimal, and the translation of sentences proved to be of high quality, showcasing the effectiveness of fine-tuning a pre-trained model.

## Conclusion
In conclusion, this project embarked on the journey of English to Hindi text translation through deep learning. The multi-part approach allowed the exploration of various models and datasets, showcasing both the challenges and successes in building translation systems. While certain parts faced overfitting issues, the utilization of different architectures and techniques yielded valuable insights into the realm of neural machine translation.

 
Source of the dataset:- 
1. https://www.cfilt.iitb.ac.in/iitb_parallel/ (https://www.kaggle.com/datasets/shirshmall/english-hindi-translation-iitb)
2. https://www.clarin.eu/resource-families/parallel-corpora (https://www.kaggle.com/datasets/aiswaryaramachandran/hindienglish-corpora)

Kaggle Notebooks:-

Part 1: https://www.kaggle.com/code/shirshmall/english-to-hindi-translation-attention-model/notebook

Part 2: https://www.kaggle.com/code/shirshmall/english-to-hindi-translation-transformer/notebook

Part 3: https://www.kaggle.com/code/shirshmall/english-to-hindi-translation-fine-tune-huggingface
 
