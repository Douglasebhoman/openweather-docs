# Reading the Response

A successful request returns an HTTP **200** status code with a JSON 
body containing the current weather data.

## Example Response
```json
{
    "name": "London",
    "main": {
        "temp": 7.69,
        "feels_like": 5.1,
        "humidity": 93
    },
    "weather": [
        {
            "main": "Clouds",
            "description": "overcast clouds"
        }
    ],
    "wind": {
        "speed": 4.12
    },
    "visibility": 10000,
    "cod": 200
}
```

## Key Fields Explained

| Field | Description | Example |
|-------|-------------|---------|
| name | City name | "London" |
| main.temp | Current temperature | 7.69 |
| main.feels_like | Perceived temperature | 5.1 |
| main.humidity | Humidity percentage | 93 |
| weather[0].description | Weather condition | "overcast clouds" |
| wind.speed | Wind speed in m/s | 4.12 |
| visibility | Visibility in metres | 10000 |
| cod | Status code (200 = success) | 200 |

!!! tip
    The `dt` field returns the time of the data as a **Unix timestamp**. 
    You can convert it to a readable date using any online Unix converter.