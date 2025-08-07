# Pollinations-Ai-Python
Not official Python library, for working with [pollinations.ai](https://pollinations.ai/)!

# Installing
## THE LIBRARY IN DEVELOPMING!

You can install lib with pip
```bash
pip install pollinations
```

And using
```python
import pollinations
```

# Using

### WARNING!
### To use you need a api key from [auth.pollinations.ai](https://auth.pollinations.ai)

## Text Generation

```python
import pollinations


api_key = "" # Replace to you token

ai = pollinations.Pollinations(api_key=api_key, type=pollinations.Type.Text)

#Generate text

result = ai.chat.message(
    model="chatgpt4", # model id from ai.chat.models
    prompt="Hello! Who are you??", # Messsage
    system="You is a ChatGpt4 By OpenAi", #  instruction
    history={}
)

# Print result
print(result.message)
```

Text message return a json-object.
```JSON
{
"message":"..",
"api_key":"..",
"temperature":0,
"model":"..",
"system":"..",
"history":[
 {
  "role":"..",
  "content":".."
 }
]
}
```

And you using it

```python
result.message
result.api_key
..
```