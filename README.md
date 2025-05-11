# 🌦️ Weather API Fetcher using MuleSoft & Postman

This project is a simple **Weather API Application** built using **MuleSoft Anypoint Studio** and tested via **Postman**. It sends city names as input through an HTTP GET request and fetches **real-time weather data** from an external weather API source. The response includes details like temperature, humidity, wind speed, and more.

## 🔧 Technologies Used
* MuleSoft Anypoint Studio
* Postman
* REST APIs
* JSON

## 📌 Features
* 🌍 Input a city name to fetch live weather data.
* 📡 Sends a GET request to an external API to fetch weather information.
* 📦 Displays weather details in structured JSON format.
* 💡 Handles valid and invalid test cases.

## 🧪 How It Works
1. The user sends a **GET** request using **Postman**.
2. In the **Body** (raw, JSON format), the user provides a key-value pair:

   ```json
   {
     "city": "Mulbagal"
   }
   ```
3. MuleSoft reads the city name, forwards it to the external weather API.
4. The API responds with weather information such as:

   * City Name
   * Country
   * Message (status)
   * Minimum & Maximum Temperature
   * Humidity Level
   * Wind Speed

## 🧾 Example Output
```json
{
  "City_Name": "Mulbagal",
  "Country": "India",
  "Message": "Weather Details",
  "Minimum_Temperature": "31.89 Degree Celsius",
  "Maximum_Temperature": "31.89 Degree Celsius",
  "Humidity Levels": "39%",
  "Wind Speed": "1.67 KMPH"
}
```

## ✅ Test Cases

* ✅ Valid input (`Bangalore`) — receives correct weather data.
{
    "City_Name": "Bangalore",
    "Country": "India",
    "Message": "Weather Details",
    "Minimum_Temparature": "29.8 Degree Celcius",
    "Maximum_Temparature": "31.32 Degree Celcius",
    "Humidity Levels": "49 %",
    "Wind Speed": "2.06 KMPH"
}
* ❌ Invalid city name — gracefully handles error or shows proper message.
{
    "Given City Name": "",
    "Message": "Please Ensure the Correct City Name",
    "Error ": {
        "cod": "400",
        "message": "Nothing to geocode"
    }
}

