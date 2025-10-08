# Weather Alert SMS Notification 🌧️

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
   
## Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/rain-alert.git
   cd rain-alert
   ```
2. Set up environment variables: Add the following to your `.env` file or system environment variables:
   ```bash
   OWM_API_KEY="your_openweathermap_api_key"
   TWILIO_ACCOUNT_SID="your_twilio_account_sid"
   TWILIO_AUTH_TOKEN="your_twilio_auth_token"
   TWILIO_VIRTUAL_NUMBER="your_twilio_virtual_number"
   TWILIO_VERIFIED_NUMBER="your_verified_number"
   https_proxy="your_proxy_url"  # Optional, if behind a proxy
   ```
3. Update the location coordinates in the script (`lat` and `lon`) to your preferred location:
   ```bash
   weather_params = {
       "lat": 51.507351,  # Example: Latitude for London, UK
       "lon": -0.127758,  # Example: Longitude for London, UK
       "appid": api_key,
       "exclude": "current,minutely,daily"
   }
   ```

## How to Use
1. Run the script:
   ```bash
   python script_name.py
   ```
2. If rain is expected, the script will send an SMS notification to the verified phone number.

## Example Output
If rain is expected:
   ```bash
   Message sent! Status: queued
   ```
If no rain is expected:
   ```bash
   No rain expected today.
   ```

## Error Handling
- The script validates the API responses and raises an exception if an error occurs.
- Includes error handling for Twilio's SMS sending process.  

## License
This project is created for educational purpose.
