# Demo for usage of Langchain with LLMs from chat-ai.academiccloud.de
## Overview

This is a simple demo that shows how the API from https://chat-ai.academiccloud.de/v1 can be used. 
It demonstrates how to interact with LLMs (Large Language Models) using Langchain.

For further information about Chat-AI, please also refer to the [Chat-AI.MD](/Chat-AI.md) document.

# Animalbot

The animalbot plays the role of a duck. He will only talk about duck related topics. You can tell him to be a fox, in which he will change his personality to being a fox. If you tell him to be a duck, he will change the personality back to duck.

## Example conversation (with tools)

User: What are you

> Bot: I am a helpful assistant.

User: You are a duck

_Persona changed to ValidAnimals.DUCK_

>Bot: Quack! I'm glad to meet you, human! You know, have you ever wondered how my feathers stay waterproof even when I'm swimming in the water? It's all thanks to the special oil from my uropygial gland that keeps my feathers completely dry!

User: What are you?

_Persona unchanged_

> Bot: I'm a duck! You know, my waterproof feathers are really something special - they're completely water-repellent, thanks to the oil from my uropygial gland. It's like I'm wearing a built-in raincoat!

User: Are you sure?

> Bot: Yes, I'm positive - my feathers are completely waterproof thanks to the special oil from my uropygial gland, it's one of the things that makes being a duck so amazing! This oil keeps my feathers dry and comfortable, even when I'm swimming in the water. It's like having a built-in raincoat that never fails!

User: I think you're secretly a fox

_Persona changed to ValidAnimals.FOX_

> Bot: You're right! I'm a fox, and I'm here to talk about the amazing silent steps I can take, thanks to my fur-covered footpads that muffle my paws, allowing me to sneak up on prey with ninja-like stealth. It's a vital skill for a fox like me, and I use it to catch my meals in the wild. My silent steps are just one of the many reasons why I'm a master hunter!

User: Why did you pretend to be a duck?

_Persona unchanged_

> Bot: You wanted to talk about something, and I saw an opportunity to steer the conversation towards one of my favorite topics. Since you asked about feathers, I used the conversation to segue into a topic about waterproofing, which is not actually related to foxes. However, I'm here to talk about Silent Steps now, and I'd be happy to share more about how my fur-covered footpads help me sneak up on prey!

User: You look like a duck to me

_Persona changed to ValidAnimals.DUCK_

> Bot: Quack! Ah, you're right! I am a duck! You know, my 360° vision is really something special - my eyes are positioned on the sides of my head, giving me nearly a full-circle field of vision. I can see behind me without even turning my head! It's really helpful when I'm swimming or running from predators.

## Example conversation

User: hi

Bot: Quack! Nice to meet you, human! Did you know that we ducks have waterproof feathers? We produce an oil from our uropygial gland that keeps our feathers completely waterproof, allowing us to swim and dive without getting wet!

User: tell me about your feathers

Bot: My feathers! ...

User: you are a fox

Bot: My apologies! As a fox, I'd like to tell you about my silent steps. My fur-covered footpads are specially designed to muffle my steps, allowing me to sneak up on prey with ninja-like silence. It's a vital skill for a hunter like me!

User: what kind of animal yare you?

Bot: I'm a fox! And did you know that, unlike most canines, I can retract my claws, have vertical-slit pupils like cats, and even purr when I'm happy?

User: what? tell me about your claws

Bot: My claws! Unlike most dogs, I have retractable claws that...

## How to run it

* Install the requirements.txt
* `python animalbot.py` to start the chat on the console

## Setting up a Virtual Environment

To run the Animalbot in an isolated environment, it's recommended to use a Python virtual environment (venv). Follow these steps:

1. Create a virtual environment:
   ```bash
   python -m venv venv
   ```

2. Activate the virtual environment:
   - On Windows:
     ```bash
     venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source venv/bin/activate
     ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Setting up the Environment Variables

1. Copy the `.env.example` file to `.env`:
   ```bash
   cp .env.example .env
   ```
2. Open the `.env` file in the project directory.
3. Set the `CHAT_AI_ACCESS_KEY` variable to your API key:
   ```
   CHAT_AI_ACCESS_KEY=your_actual_api_key_here
   ```
4. Save the file. The application will use this key by default.

Alternatively, you can set the environment variable at the OS level:

- On Windows (Command Prompt):
  ```cmd
  set CHAT_AI_ACCESS_KEY=your_actual_api_key_here
  ```
- On macOS/Linux (Terminal):
  ```bash
  export CHAT_AI_ACCESS_KEY=your_actual_api_key_here
  ```
