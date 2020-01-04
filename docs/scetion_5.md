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

**Custom Payloads** are used if you want to for example use multiple buttons. How to add another button is explained further down.

These Response possibilities depend on which platform you are responding to (Facebook Messenger, Skype, ...)

#### Using Custom Payloads to add a button:

Choose Custom Payload under Facebook Messenger Reply and paste following instead of the given attachment object.

````
    "attachment":{
      "type":"template",
      "payload":{
        "template_type":"generic",
        "elements":[
           {
            "title":"Welcome!",
            "image_url":"https://petersfancybrownhats.com/company_image.png",
            "subtitle":"We have the right hat for everyone.",
            "default_action": {
              "type": "web_url",
              "url": "https://petersfancybrownhats.com/view?item=103",
              "webview_height_ratio": "tall",
            },
            "buttons":[
              {
                "type":"web_url",
                "url":"https://petersfancybrownhats.com",
                "title":"View Website"
              },{
                "type":"postback",
                "title":"Start Chatting",
                "payload":"DEVELOPER_DEFINED_PAYLOAD"
              }              
            ]      
          }
        ]
      }
    }
````

You might want to change the code a little so it fits for your purposes. If you want to add buttons you can do that by adding a button (copy & paste) into the buttons array.

In the example above there are already different types of buttons from facebook. You can find all the types at https://developers.facebook.com/docs/messenger-platform/send-messages/buttons. The documentation of facebook in general is pretty good so if you ever need something, lookup there. But the Facebook Messenger is limited to a max of 3 buttons, so keep that in mind.
