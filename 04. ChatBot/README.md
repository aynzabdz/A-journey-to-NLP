<h1 align = "Center">Building a Chatbot</h1>

A chatbot is software that simulates human-like conversations with users via text messages on chat. 
In this project the aim is to create a Chatbot for an online bookshop that interacts with natural language using PyTorch.

<h2>Built With</h2>:
<ul>
  <li>NumPy</li>
  <li>NLTK</li>
  <li>PyTorch</li>
  <li>sklearn</li>  
</ul>
  
  
<h2>Intents</h2>
This chatbot is using predefined answers to interact with humans. It has a set of tags that classifies user's potential questions. 
These intents are saved in <i>intents.json</i> file. An entry in this file looks like below:

```
        {
            "tag" : "greeting",
            
            "patterns" : ["hi",
                          "hello",
                          "hi there!",
                          "is anyone there?",
                          "hey",
                          "are you there?",
                          "good day!"],
            
            "responses" : [ "Oh hey",
                            "Hello there!",
                            "Hi. How can i help you?",
                            "Hey, would you like to be assisted?"]
        }
```
"tag" refers to the class of user's potential question. "patterns" is a list consisting of some examples of sentences that are belonging to this class
and finally "responses" are just a set of potential responses to user's question. Eventually after the chatbot decides that the user's question lies 
in a specific category, it will just choose a random response and show it to user.

<h2>Approach</h2>
We need a model that decides the category of user's input. Since this chatbit model is a simple one, a <b>Feed Forward Neural Network</b> will do
more than enough. We expect the neural net to be able to predict the tag of user inputs. We can use the "patterns" in the <i>intents.json</i> file 
that we saw earlier as a training set of user input and the corresponding tags to be the target classes.

<h2>Preprocessing</h2>
We will do a simple preprocessing on the training data. This includes:
<ul>
    <li>Removing punctuation</li>
    <li>Lowering each character so we will deal with fewer words</li>
    <li>Tokenizing</li>
    <li>Stemming</li>
</ul>

<h2>Exctracting Features</h2>

In order to extract a feature set from the cleaned sentences, we use a TIFDF-vectorizer. In this project, the implementation from <b>sklearn</b> is used.

<h2>Model Training</h2>
After the features are selected and we have a nice numeric dataset, we can use a model to solve this problem. Here a simple classifier
with 1 hidden layers is chosen. Then we can train the model and interactively chat with the chatbot.
<br>
<br>
<br>
<p align="center"><b>The last cell in implementation is to interact with chatbot</b></p>
