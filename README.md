# Sentiment-Analysis-Using-LSTM
Sentiment Analysis for Amazon Fine Food Reviews Using an LSTM Model.
<br/>

In our project, which used the Amazon Fine Food Reviews dataset
(https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews),
I chose a Long Short-Term Memory (LSTM) network for sentiment analysis because LSTMs are particularly well-suited for sequential data like text, where understanding word dependencies and contextual information is crucial. LSTMs improve upon traditional RNNs by effectively retaining long-term dependencies and avoiding the vanishing gradient problem, making them excellent at capturing complex patterns in user reviews.
<br/><br/>

Preprocessing and Optimization:
To prepare the dataset, I tokenized the reviews, reduced the vocabulary to 10,000 words, and padded the sequences to a fixed length of 100 tokens to ensure uniform input lengths. This approach reduces model complexity and ensures efficient computation while preserving essential data patterns.
<br/><br/>

Model Architecture:
The LSTM model begins with an Embedding layer, which converts each word into a dense vector representation, capturing its semantic meaning. This is followed by an LSTM layer with 128 units, which processes the input sequentially and retains important contextual sentiment. A Dense layer with ReLU activation further enhances feature extraction, followed by a Dropout layer (rate = 0.5) to prevent overfitting by randomly deactivating neurons during training. Finally, a Dense output layer with sigmoid activation is used to perform binary sentiment classification.
<br/><br/>

Training and Optimization:
The model was compiled using the Adam optimizer for faster and more stable convergence. To improve efficiency, I used Early Stopping to halt training when no significant improvement in validation loss was observed, preventing overfitting and reducing unnecessary computations. The model was trained over 5 epochs with a batch size of 64.
<br/><br/>

Performance Evaluation:
The model achieved outstanding performance on the test set, with an accuracy of 93.72%. For positive sentiment classification, it attained a precision of 95%, recall of 97%, and an F1 score of 96%, demonstrating its strong ability to identify sentiment in real-world data. The inference time of just 35ms per review makes the model highly suitable for real-time applications.
<br/><br/>

Classification Report Highlights:

Negative (0): Precision = 0.88, Recall = 0.82, F1-score = 0.85

Positive (1): Precision = 0.95, Recall = 0.97, F1-score = 0.96

Macro Avg: Precision = 0.92, Recall = 0.89, F1-score = 0.90

Weighted Avg: Precision = 0.94, Recall = 0.94, F1-score = 0.94
<br/><br/>

In Conclusion:
The LSTM model efficiently captures sentiment from text reviews, offering valuable insights for customer sentiment analysis. Its robust accuracy, fast inference time, and ability to handle long-term word dependencies make it a practical solution for e-commerce platforms, review monitoring systems, and business intelligence tools.
