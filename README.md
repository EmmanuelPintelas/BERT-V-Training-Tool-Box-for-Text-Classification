# BERT-V-Training-Tool-Box-for-Text-Classification

The proposed NLP text classification framework is based on pre-trained BERT architecture in order to extract features from raw text data, feeding them into Fully-Connected (FC) neural networks in order to classify the client’s hotel review text into “Bad”, “Good”, or “Excellent” preference. 

Moreover, we developed a Validation (V) algorithm in order to efficiently train the NLP model. During training we totally froze (no updates in network weights) the first 150 layers of BERT backbone while we unfroze (let the network update its weights) its last 50 layers. The first layers remain frozen in order to avoid overfitting and catastrophic forgetting of pre-trained network’s weights, while the last layers will fine-tune with respect to our hotel text reviewing classification task. 
  
The proposed validation algorithm mainly updates the learning rate of the training procedure with respect to the validation accuracy. Also, if no further improvement is performed, the model weights are switched back into the ones who managed to bring the highest latest score. This is performed in order to avoid local optimum solutions by finding the optimum network weights parameters which maximizes the final performance score.
  
We compared the BERT-V with:

  TfidfVectorizer, RNNs, Transformer, BERT.
  
  The training-testing implementation links are in:
  
  https://www.kaggle.com/code/emmanuelpintelas/bert-training-tool-box-for-text-classification?scriptVersionId=123014179
  
  https://www.kaggle.com/code/emmanuelpintelas/transformer-rnn-tool-box-for-text-classification/notebook
  
  https://www.kaggle.com/code/emmanuelpintelas/tfidfvectorizer-tool-box-for-text-classification?scriptVersionId=123031159
  
  

