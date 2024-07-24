# GenerativeAI
## Intriduction
Text classification plays a pivotal role in numerous real-world applications, spanning from sentiment analysis and spam detection to news categorization and customer service automation. In an era where vast amounts of textual data are generated daily across various platforms such as social media, e-commerce websites, and news outlets, the ability to automatically categorize and extract insights from this data is invaluable.

This project based on Text classification based on sentiment, which involve identifying and categorizing sentiments expressed in textual data, that whether the text or post is normal or hatespeech.Abusive language has become a perpetual problem in today’s online social media. An ever-increasing number of individuals are falling prey to online harassment, abuse and cyberbullying.

The project is divided into 2 parts to identify the text that whether the text is abusive or normal.

1Representational models In the representational part I took 2 models one is "bge-large-en-v1.5"(One of the best encoders for text classification according to MTEB) and "distilbert-base-uncased" model and on top of the returned embeddings, train a logistic regression classifier with 100 maximum iterations and then evaluate the model performance.

2.Generative LLMs In generative part I Used "llama-2-chat-7B" and "zephyr-alpha-7B" and used multiple prompt from the paper Roy et al., 2023 and then evaluate the model performance and Compare a batch of representational and generative models.
