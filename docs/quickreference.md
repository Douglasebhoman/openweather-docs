# Quick Reference

A handy summary of everything you need to use the OpenWeather API.

## Base URL
```
https://api.openweathermap.org/data/2.5/weather
```

## Full Request Example
```
https://api.openweathermap.org/data/2.5/weather
  ?q=London,uk
  &appid=YOUR_API_KEY
  &units=metric
```

## Required Parameters

| Parameter | Description |
|-----------|-------------|
| q | City name (e.g. London or London,uk) |
| appid | Your API key |

## Optional Parameters

| Parameter | Description | Default |
|-----------|-------------|---------|
| units | metric / imperial / standard | standard |
| lang | Language for descriptions | en |
| lat & lon | Coordinates instead of city name | — |

## Status Codes

| Code | Meaning |
|------|---------|
| 200 | Success |
| 401 | Invalid API key |
| 404 | City not found |
| 429 | Rate limit exceeded |
| 500 | Server error |

## Useful Links

- [OpenWeather API Docs](https://openweathermap.org/current)
- [Your API Keys](https://home.openweathermap.org/api_keys)
- [OpenWeather Pricing](https://openweathermap.org/price)

!!! tip
    Bookmark this page for quick access whenever you are working 
    with the OpenWeather API!