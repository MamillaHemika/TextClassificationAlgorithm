# TextClassificationAlgorithm
Text Classification Algorithm
Follow these steps:
1.	Install Required Libraries:
Make sure you have pandas and scikit-learn installed. You can install these using pip:
pip install pandas scikit-learn
2.	Prepare the Data:
You need to organize your sentences and their corresponding labels. For simplicity, let’s assume you label them based on topics, such as Nature, Technology, Health, etc.

import pandas as pd

sentences = [
    # Your sentences here as listed above
]

labels = [
    'Nature', 'Nature', 'Technology', 'Education', 'Animal', 'Art', 
    'Economy', 'Sports', 'History', 'Food', 'Travel', 'Health', 
    # Repeat labels corresponding to your sentences
]

data = pd.DataFrame({'Sentence': sentences, 'Label': labels})


3.	Splitting the Data:
Split the data into training and testing sets.
from sklearn.model_selection import train_test_split
X = data['Sentence']
y = data['Label']
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
