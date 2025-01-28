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
- After I changed the temperture up to 1.0, it took way longer to generate its response so I decided to chnage it back for 0.5