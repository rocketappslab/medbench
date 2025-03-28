```python
from openai import OpenAI
api_key = "xxxxxxxx"
base_url = "https://az.gptplus5.com/v1"
path = "qwen-max"
question = "你好"

client = OpenAI( api_key=api_key, base_url=base_url, )

completion = client.chat.completions.create(model=path, messages=[{'role': 'user', 'content': question}])
response = json.loads(completion.model_dump_json())
print(response['choices'][0]['message']['content'])
```
