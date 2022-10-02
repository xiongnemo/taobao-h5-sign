# taobao-h5-sign
Javascript signature generator for taobao H5 apis.

## Build

```bash
# sudo npm i -g vercel
# vercel login
vercel dev
```

## Usage

Send request with string_to_sign from Taobao.

* Set `Content-Type` to `text/plain`.

```python
string_to_sign = f'{token}&{timestamp}&{APP_KEY}&{query_data_json_str}'
sign = requests.post('http://127.0.0.1:3000/api/sign', headers={"Content-Type": "text/plain"}, data=string_to_sign.encode('utf-8'))
print(sign.text)
```

Deployed [here](https://taobao-h5-sign.vercel.app/api/sign)
