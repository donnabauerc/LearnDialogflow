### Section 5: Rich messages - 3.1.2020

Modern Chatbots often also use more than just Response per Intent. There are also multiple types of Responses. -> **Rich Messages**

+ add intent:
  + name: suprise-me
  + training phrase: "suprise me"
  + Facebook Response: 
    + Text: "Here you go"
    + ...

In this video of the Tutorial we just tried the different possibilties of Facebook Messenger Responses

**Images** can't be uploaded directly to Dialogflow. Pictures have to be stored seperately like a own server or free hosting possibility

**Quick** replies need to be at the end of one Response to appear for the user,else the option isn't displayed because another response is already triggered.

**Cards** are templates from Facebook. You could for example send a link to buy something. You get an image, a button and text.Facebook also displays multiple cards as one carousel to the user, which in most of the cases is also prettier than seperate messages.

**Custom Payloads** are used to send specific JSON-Objects, mostly depending whome or what you are communicating with (further applications ...)

These Response possibilities depend on which platform you are responding to (Facebook Messenger, Skype, ...)