# Weather-Data-Fetcher-requests-
# Weather Details Fetcher

## Description
This is a **Python script** that fetches the current weather details of any city using the **OpenWeatherMap API**. The script takes a city name as input and retrieves weather data such as temperature, atmospheric pressure, humidity, and a brief description of the weather.

---

## Features
- Fetches weather data for any valid city name.
- Provides details such as:
  - Temperature (in Kelvin)
  - Atmospheric pressure (in hPa)
  - Humidity (in percentage)
  - Weather description (e.g., clear sky, rain, etc.)
- Error handling for invalid city names.

---

## Requirements
### Prerequisites
1. **Python**: Version 3.x or above.
2. **Requests Library**: Install it using:
   ```bash
   pip install requests
   ```
3. **OpenWeatherMap API Key**: Sign up at [OpenWeatherMap](https://openweathermap.org/) to get your free API key.

---

## How to Run
1. **Obtain API Key**: 
   - Create a free account on [OpenWeatherMap](https://openweathermap.org/).
   - Generate an API key from your account dashboard.

2. **Update the Script**:
   - Replace the placeholder `"Your_API_Key"` in the code with your actual API key.

3. **Run the Script**:
   - Open a terminal or command prompt.
   - Navigate to the directory containing the script.
   - Run the script using:
     ```bash
     python weather_fetcher.py
     ```

4. **Provide Input**:
   - Enter the name of the city when prompted.

5. **View Output**:
   - The script will display the current weather details for the entered city.

---

## Example Usage
### Input:
```
Enter city name: London
```

### Output:
```
Temperature (in kelvin unit): 285.15
Atmospheric pressure (in hPa unit): 1012
Humidity (in percentage): 81
Description: light rain
```

### If the city is not found:
```
City Not Found
```

---

## Customization
- **Change Temperature Unit**:
  - By default, the API returns the temperature in Kelvin. To fetch the temperature in Celsius, append `&units=metric` to the API URL:
    ```python
    complete_url = base_url + "appid=" + api_key + "&q=" + city_name + "&units=metric"
    ```
  - For Fahrenheit, use `&units=imperial`.

- **Additional Data**:
  - The OpenWeatherMap API provides other data such as wind speed, sunrise/sunset times, etc. You can extract these details from the JSON response.

---

## Error Handling
- The script checks for invalid city names and displays a **"City Not Found"** message if the API returns an error.
- Make sure the API key is valid and not expired.

---

## Notes
- Ensure your internet connection is active while running the script.
- The free version of the OpenWeatherMap API may have limits on the number of API requests per minute.

---

## License
This project is open-source and can be used freely for educational or personal purposes.

---

Let me know if you need help with further improvements or hosting this script!
