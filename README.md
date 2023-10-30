# Currency_Converter_ChatBot
The Currency Conversion Chatbot is an intelligent virtual assistant designed to facilitate real-time currency conversion for users.Developed with Dialogflow, this chatbot enables users to engage in natural language conversations, providing precise and current currency conversion rates and making currency conversions a breeze.

# ChatBot Architecture:

Architecture of the Currency Conversion Chatbot using Dialogflow and Telegram:

1.	User Interaction:
   
   	Users engage with the chatbot on the Telegram platform by sending messages such as "Convert 100 USD to EUR" or inquiring about exchange rates like "What's the current USD to GBP exchange rate?"

2.	Dialogflow:
   
   •	Intent Recognition: Dialogflow identifies user intents like "CurrencyConversion" based on their input. It also extracts essential information, like the source currency, target currency, and the amount 
      from the user's query.
   •	Context Management: Contexts are utilized to maintain the conversation's flow and enable the chatbot to remember prior user interactions.

3.	Fulfillment:
   
     Webhook Integration: When an intent is triggered, Dialogflow initiates a webhook request to your Flask application.

4.	Flask Application:
	
    •	Your Flask application functions as the fulfillment endpoint.
    •	It receives the webhook request from Dialogflow, containing user intent, entities, and context.
    •	The application uses this data to perform currency conversion by interacting with external currency exchange APIs.
    •	It computes the converted amount and prepares a response.

5.	External APIs:
   
    Currency Exchange API: Your Flask application interfaces with external currency exchange APIs to retrieve real-time currency conversion rates.

6.	Flask Application Response:
    
    Once your Flask application calculates the converted amount, it sends a JSON-format response back to Dialogflow.

7.	Dialogflow Response:
    
    •	Dialogflow processes the response from the Flask application.
    •	It generates a reply to the user, which may include the converted amount, a confirmation message, or an error message.

8.	Telegram Integration:
    
    •	Dialogflow is seamlessly integrated with the Telegram platform.
    •	When Dialogflow generates a response, it's promptly delivered to the user on Telegram as a reply to the user's original message.


    
