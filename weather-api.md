Weather API Documentation

Overview

The Weather API allows users to retrieve real-time weather information for a specified city. It provides details such as temperature, weather conditions, and location-based data.

Base URL
https://api.weather.com
Endpoint
GET /weather

This endpoint retrieves current weather data for a given city.

Request Parameters
Parameter	Type	Required	Description
city	string	Yes	Name of the city (e.g., Delhi)
Request Example
GET https://api.weather.com/weather?city=Dehradun

Response Example
{
  "city": "Dehradun",
  "temperature": "25°C",
  "condition": "Cloudy",
  "humidity": "60%",
  "wind_speed": "10 km/h"
}

Error Handling
Status Code	Message	Description

400	Bad Request	Missing or invalid parameters

404	City Not Found	City does not exist in database

500	Server Error	Internal server issue

Authentication (Optional Section – Add for better impression)

This API may require an API key for authentication.

Example:

GET /weather?city=Dehradun&api_key=YOUR_API_KEY
