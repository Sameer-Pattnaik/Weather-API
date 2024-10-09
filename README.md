### Documentation for Weather App

#### Overview
This project is a simple weather application that fetches real-time weather data for a given city using the OpenWeatherMap API. It allows users to search for a city and displays information such as the current temperature, weather conditions, highs, and lows. 

#### Files Included
1. **index.html**: Contains the HTML structure of the application.
2. **script.js**: Handles the JavaScript logic to fetch weather data and update the UI dynamically.

---

### 1. `index.html`
This is the main HTML file that provides the layout and structure of the weather app.

#### Key Sections:

- **HTML Structure**:
    - `#app`: The container for the entire weather application.
    - `#searchBar`: A search bar where the user enters the city name.
    - `#info`: Displays the current date and the city name.
    - `#tempImg`: Displays an icon representing the weather condition (e.g., cloudy, sunny).
    - `#description`: Shows a brief description of the current weather (e.g., "Clear", "Cloudy").
    - `#temp`: Displays the current temperature.
    - `#extrainfo`: Displays the high and low temperatures.

#### CSS Styles:
- The app uses a combination of flexbox and centered content.
- Gradient background in shades of blue and purple provides a visually appealing effect.
- Text styles are simple, focusing on clear visibility with light colors against the background.

---

### 2. `script.js`
This file contains the JavaScript code that powers the functionality of the weather app. 

#### Key Functions:

1. **DOM Elements**:
    - Several HTML elements like `city`, `temp`, `description`, etc., are retrieved using `document.getElementById` for dynamic updates after fetching weather data.

2. **Date Setup**:
    - The current date is displayed by constructing the day, month, and year using JavaScript's `Date` object.

3. **getWeather Function**:
    - This function is the core of the application. It gets triggered when the search button is clicked.
    - It fetches data from the OpenWeatherMap API using the entered city name.
    - Displays:
      - City name
      - Weather description
      - Icon image corresponding to the weather condition
      - Current temperature
      - Maximum and minimum temperatures
    - In case of an error (e.g., city not found), it logs the error in the console.

#### API Integration:

- The app uses the OpenWeatherMap API to fetch weather data. The API endpoint used is:
    ```
    https://api.openweathermap.org/data/2.5/weather?q=${cityName},&APPID=YOUR_API_KEY&units=metric
    ```
    Replace `YOUR_API_KEY` with a valid API key from OpenWeatherMap.

---

### How to Use:
1. Open `index.html` in a browser.
2. Enter the name of a city in the search bar and click the search icon.
3. The app will fetch and display the weather data for the entered city, including:
   - The city name
   - Weather description
   - Weather icon
   - Current temperature, high, and low temperatures.

---

### Future Improvements:
1. **Error Handling**: Add better user-facing error messages (e.g., "City not found").
2. **Responsive Design**: Improve the layout for different screen sizes.
3. **Loading Indicator**: Add a loading spinner while the data is being fetched.
4. **Additional Data**: Show more details like humidity, wind speed, etc.

This completes the basic documentation of the Weather App project!
