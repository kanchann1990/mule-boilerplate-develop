Mule API starter project template

This Template API is a mule api project template that you can use as a starting point for development of your own implementation with chatGPT.

ChatGPT is a computer program that can talk with people like you and me by understanding our messages and responding with relevant information. It has been trained on a vast amount of text data to be able to answer questions and carry out conversations on a wide range of topics. In simple terms, it’s a virtual assistant that can chat with you!

We can integrate mulesoft with chatGPT as well. 

For that we need to setup ChatGPT API Key

Generating API Key::

We first need to create an account with OpenAI and obtain an API key. Once we have our API key, we can use it to authenticate our requests to the ChatGPT API.

Steps:

1. Create an openAI account: To get started with OpenAI, you need to create an account by going to the OpenAI website and signing up (https://chat.openai.com/).
2. Create a new API key: Once you have logged in to your OpenAI account, go to the (https://platform.openai.com/overview) “API keys” section of your dashboard, and click the “Create API key” button.
3. Create Key: Click the “Create a new secret key” button to create the API key. A key will be generated ,Copy it to use it in your application.


MuleSoft Integration with ChatGPT API

Sample request which needs to be sent to chatGPT API which contains model name and messages 

{
    "model": "gpt-3.5-turbo",
    "max_tokens": 128, //optional by default openAPI uses 2048 token
    "n": 3,
    "messages": [
        {
            "role": "user",
            "content": payload.query
        }
    ]
}

In the context of the OpenAI specification:

model: The "model" refers to the specific language model that will be used to generate the text response to the user's input. In this example, the model being used is "gpt-3.5-turbo", which is a version of the GPT language model architecture that has been optimized for speed and efficiency.
max_tokens: The "max_tokens" parameter specifies the maximum number of tokens (words or symbols) that the model will generate in response to the user's input. In this example, the value is set to 128, which is lower than the default value of 2048 tokens used by OpenAI.
n: The "n" parameter is used to generate number of response.
messages: The "messages" parameter contains an array of objects that represent the user's input and the model's response. In this example, there is only one message, The model will generate a response based on the input and return it to the user.
role: The "role" can be either "system", "user", or "assistant"
content: The "content" of message which is passed to our api 



Ref: https://medium.com/@nitinprakash05/mulesoft-integration-with-chatgpt-26bdb3774a4f