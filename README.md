# MedBench_API_test
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
    "temperature": temperature,
    "top_p": top_p,
    "top_k": top_k
})
headers = {
    'Content-Type': 'application/json',
    'X-HW-ID': 'APP_Z07IX2_RUNDA_20250417',
    'X-HW-APPKEY': '6aalJuNqNSMPonXEis+S0g=='
}
response = requests.request("POST", url, headers=headers, data=payload, verify=False)
#print("data is ", response.text)
response = response.json()
out = response['choices'][0]['message']['content']
