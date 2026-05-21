Solar Radiation – Project Briefing
 What does this project do?
This ESP32-C3 project connects to the internet and retrieves live solar and weather data for Cape Town using an online weather service.
The data is then displayed on a 128×64 OLED screen and automatically updates every 5 minutes.
________________________________________
What is solar radiation?
Solar radiation is the amount of sunlight energy reaching the Earth’s surface, measured in watts per square meter (W/m²).
• Low values → cloudy or early morning/evening
• High values → clear sky, strong sunlight (around midday)
• Typical clear-sky maximum ≈ 1000–1100 W/m²
This value is important for:
• Solar panel performance
• Weather analysis
• UV exposure and heat studies
________________________________________
Where does the data come from?
The project uses the Open-Meteo API, a free online weather service.
Requested live data:
•  Temperature (°C)
•  Relative Humidity (%)
•  UV Index
•  Shortwave Solar Radiation (W/m²)
The API URL includes:
• Latitude: -33.925
• Longitude: 18.4241
(Your real Cape Town location)
________________________________________
 How the system works (step-by-step)
1. ESP32 starts
o Initializes I²C for the OLED (SDA = GPIO 7, SCL = GPIO 6)
o Initializes Wi-Fi
2. Connects to Wi-Fi
o Displays connection status on the OLED
3. Requests online data
o Sends an HTTP request to Open-Meteo
o Receives a JSON response
4. Processes the data
o Extracts temperature, humidity, UV index, and radiation
5. Displays results
o Shows all values clearly on the OLED screen
6. Automatic updates
o Data refreshes every 5 minutes without restarting the device
________________________________________
 What appears on the OLED?
SOLAR WEATHER
Radiation: 1078 W/m2
UV Index: 9.0
Temp: 22.9 C
Humidity: 54 %
This gives a real-time snapshot of solar and atmospheric conditions.
________________________________________
 Why is this project educational?
This project teaches students:
• How microcontrollers access real online data
• Basics of IoT (Internet of Things)
• Understanding solar energy and UV exposure
• JSON data parsing
• Displaying sensor-like data without physical sensors
 No physical solar sensor is required — the ESP32 acts as a smart data terminal.
________________________________________
 Key takeaway
The ESP32 is not measuring sunlight directly — it is fetching real scientific data from the internet and presenting it locally in real time.
This mirrors how many professional weather stations and dashboards work.
