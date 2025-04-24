# MedBench_API_test
```python
url = "https://apigw-cn-south02.huawei.com/api/v1/chat/completions"
payload = json.dumps({
    "model": "readypangu3832k",
    "messages": [
        {
            "role": "user",
            "content": problem
        }
    ],
    "n": 1,
    "max_tokens": 4096,
    #"repetition_penalty": 1.0,
    "temperature": 0.3,
    "top_p": 1.0,
    "top_k": 1
})
headers = {
    'Content-Type': 'application/json',
    'X-HW-ID': 'APP_Z07IX2_RUNDA_20250417',
    'X-HW-APPKEY': 'xxxxxxxxxxxxxxxxxxx'
}
response = requests.request("POST", url, headers=headers, data=payload, verify=False)
#print("data is ", response.text)
response = response.json()
out = response['choices'][0]['message']['content']
```
