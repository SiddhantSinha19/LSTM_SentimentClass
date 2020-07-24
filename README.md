# SentiSid
This is Sentiment Classification task using LSTM architecture of RNN

This model uses pre-trained gloVe embeddings of 4,00,000 words. Embeddings can be downloaded from my google drive link: https://drive.google.com/open?id=1SBeozSxq8WqzSL5hOxEkc-qPOoDE0ziR . Save embeddings in the same folder as the model code.
Also download the utils.py file and have it in the same folder as model's code 
I used the utils.py and gloVe embeddings files from the coursera course - Sequence Models (by DeepLearning.ai - by andrew Ng)
utils.py has a lot of code, but I am using only 1 function read_glove_vecs() to read the gloVe vector.

Data set contains 16 lac tweets - download from the link: https://drive.google.com/file/d/1L9EvOp9fdHsiOvYvyfvg0X3NgeRJL-hF/view?usp=sharing , which were orignally labelled 4 for positive and 0 for negative.
I changed 4 to 1, so that my labels are 0 and 1 sigmoid activtion function can be applied.
Store this data set in folder named "data" (to match the path in the code), or store according to your need and change the path in the code.

function sentence_to_indices() converts sentence to indices. Each word of the sentence is coonvert to a positive integer index and an array stores all the indices for 1 sentence. An array of array containing indices of various sentences is returned
input - ['sentence1 ...',sentence2 ...', ...]
ouput - [[indices_for_sentence1],[indices_for_sentence1],...]

pretrained_embedding_layer() - defines the pre-trained embedding layer
sentiSid() - defines the model architecture

Model uses optimizer "adam" and loss function - "binary_crossentropy"

I trained the model on 1 lac training data using a validation set of 20,000. 
Test accuracy = 76.4% was obtained.

As of now, I haven't done hyperparameter tuning, which remains as future work.

Please, cite my work, if you're using it.

For any query - write to me at sid.ronaldo1904@gmail.com

Siddhant Sinha
