# Zero_Shot_Classifier_Explainer

Zero_Shot_Classifier classifies the text that is not used in training the model. It can classufy the text withe unseen level. In simple word, here model is trained with the text without any level or class. Therefore based on the user's preferred class, the text is classified. In typical supervised classifier, the model is trained with the texts and the corresponding classes, and then it classify the text into classes. The supervised models do not cosider the contectual relation between the text and the levels. Zero_Shot_Classifier_Explainer based on the contextual relation between the text and the level it determines whether the text is related to the the class or not. 

# Example

Let's say we have the folllowing text:

"John Doe is suspected of harassing and stalking Amanda Ruiz, his former spouse. Doe is suspected of making calls and sending text and social media messages to Ruiz threatening harm to Ruiz and Ruiz’s children. Evidence of these messages and phone calls is suspected to be retained on Doe’s phone. Additionally, Doe is suspected of monitoring Ruiz online and physically at Ruiz’s workplace. Evidence of online stalking and harassment is suspected to be present via Internet History, Bookmarks, and Cookies on Doe’s phone. Evidence of physical stalking and harassment is suspected to be present through location data, calendar entries tracking Ruiz’s movements, and photos/videos taken by the Doe of Ruiz."

Zero_Shot_Classifier has classified this text related to Crime. Further, it detects the attention words that inflence the Zero_Shot_Classifier to predict this text as Crime class.

The attention words are considered as explanations to support this prediction:




Predicted  Class of the text: 
Crime

Explanation Attention Words in the text to justify the prediction:

['Additionally,', 'Ruiz’s', 'threatening', 'location', 'online', 'former', 'phone.', 'through', 'monitoring', 'History,', 'photos/videos', 'suspected', 'stalking', 'spouse.', 'sending', 'social', 'messages', 'physically', 'present', 'Bookmarks,']




# Review Data Analysis

We have applied the Zero-Shot-Classification on the Review data sets: Hotel Review and IMDB Movie Review data are collected from Kaggle. The data is available here https://drive.google.com/drive/folders/1D9vNJ9O11JOyXo89-Sl2bsguoSxB59nZ?usp=sharing

In IMDB movie data there are 50000 reviews, and in hotel data there are about 5 million reviews.

Here  the model detects the class of the review and the Zero-Shot-Explainer generates the attention words to justfy the prediction.

The sample outcomes for the hotel review:

Predicted Sentiment Class: 
Positive

Explanation Attention Words in the text to justify this prediction:

['serving', 'affect', 'comfortable', 'recommend', 'complete', 'staying', 'modesty', 'guests', 'restaurant', 'stranger', 'still', 'start', 'little', 'facilities', 'concerned', 'corner', 'black', 'practically', 'across', 'lack']


Predicted Sentiment Class: 
Negative

Explanation Attention Words in the text to justify this prediction:
['renovated', 'noise', 'no', 'noisy', 'room', 'rooms', 'people', 'building', 'currently', 'hotel']

# Code

The sentiment analysis codes are available in Zero_Shot_Classification_Sentiment_Analysis notebooks. The data should be set up along with path. Further for the sentiment analysis application the code is available in Google colab https://colab.research.google.com/drive/1rE1NIUsMOJdrkxDBVssPm_DCKUKXlIxk?usp=sharing


The explanation code is available in Zero_Shot_Classification_and_explanation_Application notebook. Further in Google Colab https://colab.research.google.com/drive/1D78McZFCjM9XDMtTsE8EfNg6lSHeKxhe?usp=sharing

# Data

The data sets are available here https://drive.google.com/drive/folders/1qziYZb0l9d-_KBIueCnWGvuVnuZr4yil?usp=sharing

# Packages need to be installed

transformers_interpret

transformers

Python-3.5






















