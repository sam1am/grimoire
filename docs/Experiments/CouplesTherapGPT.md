Prompt: 

Let's write a new app. It should connect to an sms service (pick the easiest to implement and I will sign up for it and provide credentials). Keep the config in a separate file. We need to take two ten digit US phone numbers (each associated with a name) as input. Create a new text conversation between the service and the two phone numbers. 
On the service side, any responses from the two phone numbers will be sent to openai's chat completion api. 

An example API call is as follows: 
```python
# Note: you need to be using OpenAI Python v0.27.0 for the code below to work
import openai

openai.ChatCompletion.create(
  model="gpt-3.5-turbo",
  messages=[
        {"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": "Who won the world series in 2020?"},
        {"role": "assistant", "content": "The Los Angeles Dodgers won the World Series in 2020."},
        {"role": "user", "content": "Where was it played?"}
    ]
)
```

A response looks like this: 
```
{
 'id': 'chatcmpl-6p9XYPYSTTRi0xEviKjjilqrWU2Ve',
 'object': 'chat.completion',
 'created': 1677649420,
 'model': 'gpt-3.5-turbo',
 'usage': {'prompt_tokens': 56, 'completion_tokens': 31, 'total_tokens': 87},
 'choices': [
   {
    'message': {
      'role': 'assistant',
      'content': 'The 2020 World Series was played in Arlington, Texas at the Globe Life Field, which was the new home stadium for the Texas Rangers.'},
    'finish_reason': 'stop',
    'index': 0
   }
  ]
}
```

Each message sent to the API should provide the previous 20 lines of context. The entire conversation should be kept in a text chat log including the responses from the API. 

Please ask any clarifying questions if necessary before proceeding.

