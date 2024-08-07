# Aspect-Based-Sentiment-Analysis-using-BERT

Aspect-Based Sentiment Analysis (ABSA) is a fine-grained sentiment analysis task that involves identifying the sentiment expressed towards specific aspects or features of a product, service, or entity within a text. The input typically consists of a piece of text (e.g., a review or comment) and a set of predefined aspects (such as "battery life" and "screen quality" in a product review) or features. The output is the sentiment (e.g., positive, negative, neutral) associated with each identified aspect within the text. This allows for a more detailed understanding of opinions and emotions expressed about specific aspects rather than just an overall sentiment for the entire text.

## 1. Dataset
- The dataset using in this project is the SemEval-2014 Task 4: Aspect Based Sentiment Analysis data set, specifically restaurant review comments.
- Basic preprocessing including: removing punctuation, normalizing and separating based on whitespace.
- Contains 3,041 sentences (not full reviews, but individual sentences extracted from reviews) for training set and 800 sentences for test set.
## 2. Data Preparation
- Process text data and prepares it for input into a BERT model or similar transformer models.
- Perform padding on text to ensure that all sequences are of the same length.
- Create attention masks that the model can use to ignore padding tokens during processing.
## 3. ABSA with Bert
- The ABSABert model consists of a pre-trained BERT model, including word, position, and token type embeddings, followed by 12 transformer encoder layers with self-attention and feed-forward networks.
- A pooling layer is used to extract features from the [CLS] token, which are then passed through a linear layer to predict sentiment classes. The model also includes a CrossEntropyLoss function for multi-class classification training.
- Model Evaluation: 0.811 Accuracy on test set
## 4. References
- Maria Pontiki, Dimitrios Galanis, Haris Papageorgiou, Ion Androutsopoulos, and Suresh Manandhar. "SemEval-2014 Task 4: Aspect Based Sentiment Analysis." In Proceedings of the 8th International Workshop on Semantic Evaluation (SemEval 2014), pages 27-35, 2014.
- Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. "BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding." In Proceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long and Short Papers), pages 4171-4186, 2019.
