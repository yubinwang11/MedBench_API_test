# MedBench_API_test
```python
url = "https://apigw-cn-south02.huawei.com/api/v1/chat/completions"
data = {
        "content":problem,
        "top_n_sigma": -1, 
        "top_p": 1.0,
        "top_k": 1,
        "temperature": 0.3,
        }
headers = {
    'Content-Type': 'application/json',
    'X-HW-ID': 'APP_Z07IX2_RUNDA_20250417',
    'X-HW-APPKEY': 'xxxxxxxxxxxxxxxxxxx'
}
response = requests.post(url=url, json=data, headers=headers, verify=False).json()
```
