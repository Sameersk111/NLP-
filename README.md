# NLP-
This repository has mainly a project which was worked on twitter tweets dataset with multiple models 


 
Emotion Detection in Tweets
 
NLP Course Project
 
Introduction:
 
This project is about recognizing emotions in tweets using deep learning. Given a set of tweets labeled with emotions like joy, anger, sadness, and fear, the goal is to build models that can correctly predict the emotion expressed in new, unseen tweets. This is a graded project for an NLP course, and we were asked to try three different types of models and compare their results.
 
Dataset :
 
The dataset contains lines where each tweet is followed by its emotion label, separated by a semicolon. For example: I just got a promotion;joy
We were given a training and test set to work with. A final validation set will be shared later to check how well the model performs on completely unseen data.
 
Before training, the data was cleaned and converted into a format that the models could understand. Each unique emotion was also mapped to a number so the models could process them.
 
Models Used
 
1. Fully Connected Neural Network (FCNN)
 
This was our simplest model. It turned each tweet into a vector by averaging word embeddings. Then, it passed that vector through a few layers to predict the emotion. While basic, it gave us a good starting point.
 
Training Accuracy: Around 84%
 
It worked fine, but sometimes confused similar emotions.

 
2. LSTM (Long Short-Term Memory)
 
This model handled the sequence of words better than FCNN. It processed tweets one word at a time, remembering important patterns.
 
Training Accuracy: Around 86%
 
It performed better than the FCNN, especially for emotions like fear or surprise.
 
 
3. Fine-Tuned Transformer (DistilBERT)
 
This model used a pre-trained transformer called DistilBERT. We fine-tuned it on our emotion data using the HuggingFace library. This model had already learned a lot about language, so it was able to understand even subtle emotions in tweets.
 
Training Accuracy: Over 96%
 
Best performance among all models
 
It handled all emotion categories well, even the tricky ones.
 
 
Evaluation
 
To compare the models, we looked at:
Accuracy
Precision, recall, and F1-score
 Confusion matrices
 ROC curves
 
The Transformer clearly performed the best. It was more accurate, more balanced across different emotions, and less likely to make major mistakes. The LSTM was also solid. The FCNN was okay for a basic setup but struggled with more complex emotions.
 
How to Run the Project
1. Install the required libraries: 
 pip install torch transformers datasets scikit-learn pandas matplotlib seaborn
 2. Make sure the train.txt file is in the same folder.
 3. Open and run the notebook NLP.ipynb. It includes everything — data loading, training, evaluation, and comparison of all three models.
Project Folder 

Final Note
 
This project was done as part of an NLP course. It helped us understand how different models handle text classification and showed the clear strengths of modern transformer-based models for emotion detection.
 
 

