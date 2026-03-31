# OpenWeather API Documentation

This guide was written for anyone who has never used an API before 
and wants to retrieve real, live weather data without needing a 
coding background.

The official OpenWeather documentation is written for developers. 
This guide is written for everyone else — if you can use a web 
browser, you can follow this guide.

## What You Will Learn

- How to create an OpenWeather account and get an API key
- How to make your first API request using Postman
- How to read and understand the response data
- How to recognise and fix common errors

## What You Need

- A web browser
- A free OpenWeather account
- A free Postman account
- No coding experience required

## Quick Start

Get the current weather for London:
```
GET https://api.openweathermap.org/data/2.5/weather
  ?q=London
  &appid=YOUR_API_KEY
  &units=metric
```

A successful response looks like this:
```json
{
    "name": "London",
    "main": {
        "temp": 7.69,
        "feels_like": 5.1,
        "humidity": 93
    },
    "weather": [{ "description": "overcast clouds" }],
    "cod": 200
}
```

## How This Guide Is Organised

| Section | What It Covers |
|---------|---------------|
| Authentication | How to get and use your API key |
| Endpoints | The URL structure and available parameters |
| Reading the Response | What each field in the response means |
| Error Handling | What goes wrong and how to fix it |
| Quick Reference | A one-page summary of everything |

---

!!! tip
    Never used an API before? Start with the 
    [Authentication](authentication.md) page — it takes less than 
    5 minutes to set up.