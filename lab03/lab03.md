# Prompt Engineering Process

# First attempt
- For the first attempt, I tried to send a message to the model and ask it to answer instead of having user input. After I ran it, it was an error related to role because I assigned it to be "Story Teller".

# Second attempt
- I decided to use the user input in the messages list instead of passing a message string to the model. I also change the role to "user" instead of "Story Teller".
```{'role': 'user', 'content': input('Your message: ')}```
-  I was trying to access the input from the message list by using a square brackets which gave me an attribute error. ```  print(f'homie: {response.messages[0].content}')```

# Third attempt
- The program ran after that but I was stuck in a infinite loop since I don't have any user input for the loop. 

# Fourth attempt
- After I add user input inside the loop I now finally able to talk back and forth with the AI. 
``` message = {'role': 'user', 'content': input('Your message: ')} messages.append(message) ```
- I also learn that the temperature in the options control the randomness and creativity of the model. so I decided to change it to the highest from 0.5 to 1.0, and I also change the max tokens from 100 to 80 as well.
``` options = {'temperature': 1.0, 'max_tokens': 80}`

# Fifth attempt
- After tested and made sure the model running correctly, I decided to change the role and the content of my model to fitting more of a story teller. 

  <code>
  messages = [
 {'role': 'assistant', 'content':'You should have emotions like a human\
                                and you are a person that loves telling story in a very aggresive way.'}
]
</code>

# sixth attempt (final analysis)
- I decided to change the content for the AI to be a DND game master instead. I also change the temperature down to 0.5 again because 1.0 takes too long to generate responses. After tested the AI as a game master, the outcome is really good when the story it made up is really insterested and engaging. Not only that the AI successfully narrate the story and walk me through the story with it and also gave me multiple options for me to select from. After I chose an option, it also successfully have a story that follow up my option instead of telling another story that unrelated to my choice. The user will have the chance to read through an intersting story in DND setting and also keep making choices until they decided to use the "/exit" keyword to exit out of the chat box.
