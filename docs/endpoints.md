# Endpoints

## Current Weather

The main endpoint for retrieving current weather data for any location.
```
GET https://api.openweathermap.org/data/2.5/weather
```

## Query Parameters

| Parameter | Required | Description | Example |
|-----------|----------|-------------|---------|
| q | Yes (or lat/lon) | City name | q=London |
| lat | Alternative to q | Latitude coordinate | lat=51.51 |
| lon | Alternative to q | Longitude coordinate | lon=-0.13 |
| appid | Yes | Your API key | appid=abc123 |
| units | No | Temperature unit | units=metric |
| lang | No | Response language | lang=en |

## Units

| Value | Temperature | Wind Speed |
|-------|-------------|------------|
| standard | Kelvin | m/s |
| metric | Celsius | m/s |
| imperial | Fahrenheit | mph |

## Example Request
```
https://api.openweathermap.org/data/2.5/weather
  ?q=Prague
  &appid=YOUR_API_KEY
  &units=metric
```

!!! tip
    Use **metric** for Celsius or **imperial** for Fahrenheit. 
    If you leave units out, temperatures default to Kelvin.
