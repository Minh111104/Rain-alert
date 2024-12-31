# Weather Alert SMS Notification

This Python script uses the OpenWeatherMap API to check the weather forecast for the next 12 hours and sends an SMS notification if rain is expected. The SMS is sent using Twilio.

## Features

- Fetches hourly weather data using the OpenWeatherMap API.
- Checks for rain conditions (`id` < 700) in the weather data.
- Sends an SMS alert to notify you about the rain using Twilio.
- Utilizes environment variables to securely manage API keys and sensitive information.

## Prerequisites

Before running the script, ensure the following:

1. **Python Libraries**:
   - `requests`
   - `twilio`
   
   Install them using:
   ```bash
   pip install requests twilio
