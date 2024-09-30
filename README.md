# OpenAI-API-requests
Python classes which allow using OpenAI API easily. Based fully on web requests.

The classes are well documented within the code file. 

Currently there are classes:

ChatGPTAgent - allows you to create instance (object) of ChatGPT, saves conversation history and supports tweaking all parameters like model, system prompt, temperature etc. Use GetResponse to send a new message to the chatbot, ChangeSystemMessage to change system message without affecting conversation history, and use ClearHistory to reset message history.

ImgChatGPTAgent - same as ChatGPTagent, but introduces additional method GetResponseWithImg, which allows you to send a message containing a image file. Please mind that as of now only ChatGPT 4o and 4o-mini support processing images.

DallEAgent - Allows to generate an image with DALL-E AI image generator. Use GetImage to get the image as PIL Image variable, or use GetImageURL to get link to generated image.

# Usage

To use it in your Python project, download my code into same folder and write: 

from APIWojOpenAI import * 

Of course that depends on how you name the file.

Class ChatGPTAgent should work well on embedded MicroPython systems, such as Raspberry Pi Pico. In that case remove other classes from the file and replace all import statements with import urequests as requests .
