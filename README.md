# Have-fun-with-deep-learning----pytorch-tensorflow

I'm playing with tensorflow and pytorch for LSTM model, on yelp review classification (5 categories)





Basically, the word2vec dictionary is trained in TF with architecture:

  * embedding (Embedding)        (None, 250, 64)           640000    
  * global_average_pooling1d (Gl (None, 64)                0         
  * dense (Dense)                (None, 128)               8320      
  * dense_1 (Dense)              (None, 5)                 645       

Then, load weights from word2vec into pytorch.

Finally, train Sequential model with architecture:

  * (embedding): Embedding(10000, 64)
  * (lstm): LSTM(64, 256, num_layers=2, batch_first=True, dropout=0.1)
  * (dropout): Dropout(p=0.3)
  * (fc1): Linear(in_features=256, out_features=256, bias=True)
  * (sig1): ReLU()
  * (fc2): Linear(in_features=256, out_features=5, bias=True)
  * (sm): Softmax()
  
Please check my notebook for more detailes.

BTY, you may find more interesting projects in my other repo: https://github.com/jerryzhu1/ProjectX
  


-Jerry
 
