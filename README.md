# 6obcy-mitm-python
A 6obcy MITM attack demonstration using Python.

## How this works
This script establishes two connections with strangers at the same tame and then interconnects them. Doing so allows to sniff conversations and add messages to them on-the go.

## Features

- **No web browser needed at all (uses websockets, doesn't depend on selenium)**
- Automatically connect and solve captcha (using 2Captcha API, more below)
- Store messages in a queue until second stranger connected
- Log all conversations into files
- Replicates typing states
- You can add something to the conversation on-the-go
- Save all solved captchas (in case you want to have some fun trying to crack them using machine learning)
- Properly integrates with 2Captcha API and reports both well and wrongly resolved captchas
- Changes the captcha after 3 failed solving attempts
- Object-oriented
- You can add as many client pairs as you want

## Installation
Python3 required to run.
Install the dependencies from `requirements.txt`:
```
pip3 install -r requirements.txt
```
or
```
pip3 install 2captcha-python websocket-client
```

## Usage
```
python3 main.py <YOUR_API_KEY>
```
It begins to work, saves conversations into `logs/`.
If you want to add something to the conversation, type `<NR><MESSAGE>`, for example: `1Hej k`
If you want to close the conversation, type `<NR>:q`

## Captcha solving API
This project uses 2Captcha as the captcha solving api.
Therefore, you need to specify an API key.
**NOTE: You don't actually have to pay for it with money. You can just register as a worker and solve some captchas.**
