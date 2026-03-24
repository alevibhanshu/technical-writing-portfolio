Weather API Documentation

_Overview_

The Weather API allows users to retrieve real-time weather information for a specified city. It provides details such as temperature, weather conditions, and location-based data.

_Base URL_
https://api.weather.com

_Endpoint_
GET /weather

This endpoint retrieves current weather data for a given city.

_Query Parameters_

| Parameter | Type   | Required | Description                       |
| --------- | ------ | -------- | --------------------------------- |
| city      | string | Yes      | Name of the city (e.g., Dehradun) |
| api_key   | string | Yes      | API key for authentication        |


_Request Example_

GET https://api.weather.com/weather?city=Dehradun&api_key=YOUR_API_KEY

_Response Example_

{
  "city": "Dehradun",
  "temperature": 25,
  "unit": "Celsius",
  "condition": "Cloudy",
  "humidity": 60,
  "wind_speed": 10
}


_Error Handling_

| Status Code | Error Message | Description                   |
| ----------- | ------------- | ----------------------------- |
| 400         | Bad Request   | Missing or invalid parameters |
| 401         | Unauthorized  | Invalid or missing API key    |
| 404         | Not Found     | City not found                |
| 500         | Server Error  | Internal server issue         |

_Authentication_

This API may require an API key for authentication.

Example:

GET /weather?city=Dehradun&api_key=YOUR_API_KEY
