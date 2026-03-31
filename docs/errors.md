# Error Handling

When something goes wrong, the OpenWeather API returns a short JSON 
response with an error code and a message explaining what happened.

## Common Error Responses

### 401 — Unauthorized
```json
{
    "cod": 401,
    "message": "Invalid API key."
}
```

**Cause:** Your API key is missing, incorrect, or not yet activated.

**Fix:** Double-check your API key. New keys take up to 2 hours to activate.

---

### 404 — Not Found
```json
{
    "cod": "404",
    "message": "city not found"
}
```

**Cause:** The city name you provided does not exist or is misspelled.

**Fix:** Check your spelling or use latitude and longitude coordinates instead.

---

### 429 — Too Many Requests

**Cause:** You have exceeded your plan's rate limit.

**Fix:** Wait a moment before trying again. Consider upgrading your plan 
if this happens frequently.

---

### 500 — Server Error

**Cause:** Something went wrong on OpenWeather's end.

**Fix:** Wait 30 seconds and try again. If it persists, check the 
OpenWeather status page.

## Error Code Summary

| Code | Meaning | Action |
|------|---------|--------|
| 200 | Success | Process the data normally |
| 401 | Unauthorized | Check your API key |
| 404 | Not found | Check the city name |
| 429 | Rate limit exceeded | Wait and retry |
| 500 | Server error | Retry after 30 seconds |

!!! tip
    Always check the `cod` field in every response before processing 
    the data — even if the HTTP status looks fine.