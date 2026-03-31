# Troubleshooting

A guide to the most common problems you may encounter when using 
the OpenWeather API and how to fix them.

## API Key Issues

### My key returns a 401 error immediately after creating it
New API keys take up to **2 hours** to activate. Wait and try again.

### I copied my key correctly but still get 401
Check for accidental spaces before or after the key when pasting it 
into Postman. Even one extra space will cause a 401 error.

---

## Location Issues

### The API returns the wrong city
Some city names exist in multiple countries. Add a country code to 
be specific:
```
?q=London,uk
?q=Paris,fr
?q=Prague,cz
```

### I get a 404 for a city I know exists
Try using coordinates instead of the city name:
```
?lat=50.088&lon=14.421
```

---

## Response Issues

### The temperature looks wrong
Check your `units` parameter:

| units value | Temperature format |
|-------------|-------------------|
| metric | Celsius |
| imperial | Fahrenheit |
| standard (default) | Kelvin |

### Some fields are missing from my response
Not all fields are always present. For example `rain` and `snow` 
only appear when precipitation is actually occurring.

---

## Connection Issues

### I get no response at all
- Check your internet connection
- Make sure you are using `https://` not `http://`
- Check that your firewall is not blocking the request

---

## Still Stuck?

- Check the [OpenWeather FAQ](https://openweathermap.org/faq)
- Check the [OpenWeather API Status](https://status.openweathermap.org)