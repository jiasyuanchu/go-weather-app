# Weather App

A simple weather application built with Go and Gin framework that fetches real-time weather data from OpenWeatherMap API.

## Features
- Fetches weather details such as temperature, humidity, pressure, wind speed, and description.
- Uses OpenWeatherMap API to retrieve data.
- Supports querying weather information by city name.
- Serves an HTML frontend for user interaction.

## Prerequisites
- Go (1.18 or later)
- OpenWeatherMap API Key
- [Gin Web Framework](https://github.com/gin-gonic/gin)

## Installation

1. Clone this repository:
   ```sh
   git clone https://github.com/yourusername/go-weather-app.git
   cd go-weather-app
   ```

2. Initialize and install dependencies:
   ```sh
   go mod tidy
   ```

3. Create a `.env` file and add your OpenWeatherMap API key:
   ```sh
   API_KEY=your_openweathermap_api_key
   PORT=8080
   ```

## Usage

1. Run the application:
   ```sh
   go run main.go
   ```

2. Open your browser and visit:
   ```
   http://localhost:8080
   ```

3. To fetch weather data via API, send a GET request to:
   ```
   http://localhost:8080/weather?city=London
   ```

   Example JSON response:
   ```json
   {
       "weather": [
           {
               "main": "Clear",
               "description": "clear sky"
           }
       ],
       "main": {
           "temp": 25.5,
           "feels_like": 26.0,
           "temp_min": 24.0,
           "temp_max": 27.0,
           "pressure": 1012,
           "humidity": 60
       },
       "wind": {
           "speed": 5.0
       },
       "name": "London"
   }
   ```

## Folder Structure
```
/go-weather-app
│── /static         # Static assets
│── /templates      # HTML templates
│── .env           # Environment variables (not committed)
│── go.mod         # Go module dependencies
│── go.sum         # Dependency checksums
│── main.go        # Main application file
```

## Dependencies
- [Gin](https://github.com/gin-gonic/gin) - Web framework for Go
- [godotenv](https://github.com/joho/godotenv) - Loads environment variables from `.env` file
