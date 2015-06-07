##  Meanwhile, in Python land...

```python
import requests

headers = {
   ...
}

get_response = requests.get(
    'http://api.example.com/v1/someresource',
    headers=headers
)

post_response = requests.post(
    'http://api.example.com/v1/someresource',
    headers=headers,
    body={'lol': 'super easy'}
)
```
