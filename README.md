# GenerativeAI
## Introduction
Text classification plays a pivotal role in numerous real-world applications, spanning from sentiment analysis and spam detection to news categorization and customer service automation. In an era where vast amounts of textual data are generated daily across various platforms such as social media, e-commerce websites, and news outlets, the ability to automatically categorize and extract insights from this data is invaluable.

This project based on Text classification based on sentiment, which involve identifying and categorizing sentiments expressed in textual data, that whether the text or post is normal or hatespeech.Abusive language has become a perpetual problem in today’s online social media. An ever-increasing number of individuals are falling prey to online harassment, abuse and cyberbullying.

The project is divided into 2 parts to identify the text that whether the text is abusive or normal.

1Representational models In the representational part I took 2 models one is "bge-large-en-v1.5"(One of the best encoders for text classification according to MTEB) and "distilbert-base-uncased" model and on top of the returned embeddings, train a logistic regression classifier with 100 maximum iterations and then evaluate the model performance.

2.Generative LLMs In generative part I Used "llama-2-chat-7B" and "zephyr-alpha-7B" and used multiple prompt from the paper Roy et al., 2023 and then evaluate the model performance and Compare a batch of representational and generative models.

## DATASET
The dataset used here is Hateexplain HateXplain (Mathew et al., 2021) is a benchmark dataset specifically designed to address bias and explainability in the domain of hate speech. It provides comprehensive annotations for each post, encompassing three key perspectives: classification (hate speech, offensive, or normal), the targeted community, and the rationales- which denote the specific sections of a post that influenced the labelling decision (hate, offensive, or normal).

 **hate speech:** Any speech or text that attacks
a person or group on the basis of attributes
such as race, religion, ethnic origin, national
origin, gender, disability, sexual orientation,
or gender identity.

**offensive:** The text or speech which uses abusive slurs or derogatory terms but may not be hate speech.

**normal:** The text which is neither offensive
or hate speech and adheres to social norms.**

The Dataset is splitted into 3 dictonary.
Train datasets have 15383 rows,test dataset 1924 rows whereas the validation dataset have 1922 rows.
The colums are :.
post_id : Unique id for each post.
🔹annotators : The list of annotations from each annotator.
🔹annotators[label] : The label assigned by the annotator to this post. Possible values: [Hatespeech(0), Offensive(2), Normal(1)]
🔹annotators[annotator_id] : The unique Id assigned to each annotator
🔹annotators[target] : A list of target community present in the post
🔹rationales : A list of rationales selected by annotators. Each rationales represents a list with values 0 or 1. A value of 1 means that the token is part of the rationale selected by the annotator. To get the particular token, we can use the same index position in "post_tokens"
🔹post_tokens : The list of tokens representing the post which was annotated.

