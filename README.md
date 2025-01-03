# Weather Alert SMS Notification

This Python script uses the OpenWeatherMap API to check the weather forecast for the next 12 hours and sends an SMS notification if rain is expected. The SMS is sent using Twilio.

## Features

- Fetches hourly weather data using the OpenWeatherMap API.
- Checks for rain conditions (`id` < 700) in the weather data.
- Sends an SMS alert to notify you about the rain using Twilio.
- Utilizes environment variables to securely manage API keys and sensitive information.

## Technologies Used

- **Python**: Core programming language.
- **Twilio**: For sending SMS notifications.
- **OpenWeatherMap API**: For weather forecast data.
- **Requests**: For making HTTP requests.

## Prerequisites

1. Python 3.6 or higher.
2. An account with [OpenWeatherMap](https://openweathermap.org/) to obtain an API key.
3. A Twilio account for sending SMS.
4. Installed dependencies:
   ```bash
   pip install requests twilio
   ```
   
