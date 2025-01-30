# Rockpaperscissor
# Code for rock paper scissors in machine learning through python 

import random  
from sklearn.linear_model import LogisticRegression  
import numpy as np  

# Collect user moves  
X, y = [], []  
model = LogisticRegression()  

choices = ["rock", "paper", "scissors"]  

for _ in range(10):  
    user = input("Choose rock, paper, or scissors: ").lower()  
    bot = random.choice(choices)  

  if X:  
# Train the model after first move  
   model.fit(X, y)  
     pred = choices[model.predict([X[-1]])[0]]  
    else:  
        pred = bot  

   print(f"Bot chooses: {pred}")  

  # Store move history  
  X.append([choices.index(user)])  
  y.append(choices.index(bot))
    
