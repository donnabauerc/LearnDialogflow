### Section 3: Teach chatbot to answer FAQ, Test and train the ChatBot - 17.11.2019

+ open chatbot on dialogflow:
  + create a new intent:
    + name: faq-app-more-devices
    + training phrase: "Can I use apps from the Mac App Store on more than one computer?"
    + Action: faq-add-devices
    + Fb Messenger Text Response: "Apps from the Mac App Store may be used on any Macs that you own or control for your personal user"
  + Dialogflow recognizes the word "one" as an parameter, however we don't need it now, so we delete the parameter
  + to make the bot respond to more questions than one:
    + "Can I use an app on all of my devices?"
    + "On what devices can I use the App I downloaded?"
  + After saving the intent an trying you can see, that the bot recognizes the intent even if the input is not exactly the same, as the training phrase
  + To make the bot sound more natural add response text:
    + "You can use the App from Mac Store on any device you have. No problem."
  + create new intent:
    + name: faq-delivery-time
    + traning phrases: "When will you deliver the headphones I ordered?", "When is the delivery time?", "When will my Mac be delivered?"
    + action: faq-delivery
    + Fb Messenger Text Response: "The expected time of delivery is three work days after the payment received.", "We give it our best and deliver the goods in three work days or sooner."


To test the chatbot we are going to allow friends to send the chatbot questions and get answers.
+ Open fb for developers:
  + roles/test user and add your friends

+ Bot doesn't recognize question?
  + open chatbot on dialogflow
  + history tab
  + if dialogflow couldn't find a matching intent you will see a yellow "!"
  + go back to training tab and change/create intent of the specific conversation
