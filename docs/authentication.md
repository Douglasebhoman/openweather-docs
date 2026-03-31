# Authentication

Every request to the OpenWeather API requires an API key. This key 
identifies who you are and tracks your usage.

## Getting Your API Key

1. Go to [https://openweathermap.org](https://openweathermap.org)
2. Click **Sign Up** and create a free account
3. Once logged in, click your username and select **My API Keys**
4. Copy your default key or generate a new one

!!! warning
    New API keys take up to **2 hours** to activate. If you get a 
    401 error straight away, wait and try again.

## Using Your API Key

Add your key to every request using the `appid` parameter:
```
https://api.openweathermap.org/data/2.5/weather?q=London&appid=YOUR_API_KEY
```

## Keeping Your Key Safe

- Never share your API key publicly
- Never paste it into a website or social media post
- Store it in a notes app or password manager
- If you think it has been compromised, delete it and generate a new one