# Neural_Net_Chatbot
 
## Description

In this repository, I created a simple text-based AI chatbot using Keras, Natural Language Toolkit(NLTK), and Python. Currently, the chatbot can respond to 7 different types of input, including greeting, saying goodbye, telling the user the name, age, and ability of the bot, giving user some jokes, and responding to user's praises.

 

## Files

- train.py

     This file contains the implementation and training of the model. Specifically, the first part of the file uses NLTK to transform text from intents.json to numpy arrays amd make their text and corresponded category the training samples. The second part of the file constructs a three-layers neural network using Keras that predicts which of the 7 classes the input text belongs to. After training 200 epochs, the loss and accuracy of our model are as follows:
     
     * Accuracy
     
     <img src="https://github.com/RandomY-2/Neural_Net_Chatbot/blob/main/images/chatbot_accuracy.png">
     
     * Loss
     
     <img src="https://github.com/RandomY-2/Neural_Net_Chatbot/blob/main/images/chatbot_loss.png">
     
     After train.py finishes executing, the trained model will be saved as a HDF5 file, so the user doesn't need to train the model everytime he wants to interact with the chatbot.
     
- chat.py

     This file contains the application of our trained model. Specifically, once the user executes this file, an input space will be created in terminal, and the user can type in anything(not guaranteed the chatbot can understand your text) to interact with the chatbot. The process behind the scene is that once the program recevies user's input, it will predict which category the sentence most likely belongs to, and return a random response from the category. A sample interaction is shown below:
     
     <img src="https://github.com/RandomY-2/Neural_Net_Chatbot/blob/main/images/sample_interaction.jpg">
     
     This can clearly show that our chatbot isn't perfect. Furthermore, since the chatbot has no "memory" and only returns the responses based on the predictions of inputs, it cannot have an actual "conversation" with the user. This is fair since the bot is only created using a shallow neural network. 
     
     
