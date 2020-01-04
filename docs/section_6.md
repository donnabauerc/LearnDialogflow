### Prebuilt Agents - 4.1.2020:

Prebuilt Agents are Agents which have been develeoped by Teams of Dialogflow with specific knowledge. One thing to keep in my although is that the prebuilt agents are not finished. 

You can add prebuilt agents directly via the menu under Prebuilt Agents. For example if we look at a navigation agent we can see that the intents have training phrases and parameters, but no response. 

So prebuilt agents don't specify what the bot is going to say, but they understand what the user wants, which is pretty important. You can also use one and modify it in a way, which fits for you.

#### Follow Up Intents:

Follow Up Intents are normal intents that hold the context of their parent intent. When to use follow up intents:
+ affirmatives
+ negatives
+ do later
+ cancel
+ more info
+ next or previous
+ repeat
+ number
+ custom, fallback

Create a follow up intent:

+ create entity:
  + name: Iphonexxx
  + synonyms: IphoneXXX, Latest Iphone, IPhone XXX
+ create intent:
  + name: buy.iphonexxx
  + Training phrases: "I want to buy the latest Iphone"
  + Facebook Messenger Text Response: "Would you like extended warranty for just 1 dollar availible for only this week?"
  + action: buy.iphone
+ At the overview of all intents hover above the created one & add follow up intent
  + yes: Response - "OK, great. You will receive you phone with extended warranty in 3 work days."
  + no: Response - "Ok, great. You'll receive your phone in 3 work days."

Some phrase might match more than just one intent. In that case, you can add a priority. The intent with the higher priority will be chosen first. To add a priority open up the intent you want to change and click onto the blue dot on the left side of the name of the intent.

If interested you can get a free ebook about the Tutorial in this section. Which I'm currently not going to do.