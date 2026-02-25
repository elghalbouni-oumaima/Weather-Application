# 🌦️ Weather Application

A desktop weather application developed with **PyQt5** that provides real-time current weather conditions and a 7-day forecast for any city worldwide.

The application integrates multiple APIs — OpenWeatherMap, Open-Meteo, and OpenCage — to deliver accurate and up-to-date weather data within a modern, user-friendly graphical interface.

---

## 🚀 Features

### 1️⃣ Current Weather (Page 1)

* Displays:

  * Temperature
  * Humidity
  * Atmospheric pressure
  * Visibility
  * Wind speed
  * Sunrise & sunset times
* Weather condition description with dynamic icon
* City information:

  * City name
  * Country
  * Region
  * Local time (with calendar icon)
* Temperature unit conversion (°C ↔ °F)

---

### 2️⃣ 7-Day & Hourly Forecast (Page 2)

* 7-day forecast including:

  * Daily minimum & maximum temperatures
  * Humidity
  * Weather condition icons
* Hourly forecast for the next 20 hours:

  * Temperature
  * Weather conditions
* Temperature unit conversion (°C ↔ °F)

---

### 3️⃣ City Search with Autocomplete

* Smart search bar with real-time autocomplete
* Powered by OpenWeatherMap’s geocoding API
* Displays up to 5 matching cities
* Includes country information for better accuracy

---

### 4️⃣ Modern UI Design

* Two-page layout with smooth navigation
* Custom widgets with:

  * Hover effects
  * Shadow effects
  * Weather icons
* Background image with semi-transparent overlays for enhanced readability
* Clean and intuitive user experience

---

# 🛠️ Prerequisites

* Python **3.7+**
* Required Python packages:

  * `PyQt5`
  * `requests`
  * `python-dotenv`

### 🔑 API Keys Required

* OpenWeatherMap API key (weather + geocoding)
* OpenCage API key (region details)

You can register at:

* [https://openweathermap.org](https://openweathermap.org)
* [https://opencagedata.com](https://opencagedata.com)

---

# 📦 Installation

## 1️⃣ Clone the Repository

```bash
git clone <repository-url>
cd weather-app
```

## 2️⃣ Create a Virtual Environment (Recommended)

**Windows:**

```bash
python -m venv venv
venv\Scripts\activate
```

**Linux / macOS:**

```bash
python -m venv venv
source venv/bin/activate
```

## 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

Or manually:

```bash
pip install PyQt5 requests python-dotenv
```

## 4️⃣ Configure Environment Variables

Create a `.env` file in the project root directory:

```
API_KEY=<your-openweathermap-api-key>
OPENCAGE_API_KEY=<your-opencage-api-key>
```

⚠️ Do not commit your `.env` file to version control.

## 5️⃣ Add Image Assets

Ensure the `images/` directory contains all required icon files (e.g., `sunny_icon.png`, `cloudy_icon.png`, etc.) as referenced in the `get_icone` function.

---

# ▶️ Usage

Run the application:

```bash
python main.py
```

---

## 🖥️ Application Workflow

### Page 1 — Current Weather

1. Enter a city name in the search bar.
2. Press **Search** or select a city from the autocomplete list.
3. View detailed weather information.
4. Switch temperature units using the °C/°F dropdown.
5. Click the → button to navigate to forecasts.

---

### Page 2 — Forecast

* View the 7-day forecast.
* Explore hourly predictions (next 20 hours).
* Switch temperature units as needed.
* Click the ← button to return to current weather.

---

# 📁 Project Structure

```
weather-app/
│
├── main.py          # Main application logic and GUI
├── images/          # Weather and UI icons
├── .env             # API keys (not tracked)
├── requirements.txt # Project dependencies
└── README.md        # Documentation
```

---

# 📚 Dependencies

* PyQt5 == 5.15.10
* requests == 2.32.3
* python-dotenv == 1.0.1

Install specific versions with:

```bash
pip install -r requirements.txt
```

---

# ⚠️ Important Notes

### API Rate Limits

Be aware of free-tier limits:

* OpenWeatherMap: ~1,000 requests/day
* OpenCage: ~2,500 requests/day

Frequent search input may reach these limits.

### Error Handling

* Invalid cities display `"Not Found"`.
* Some API failures may require console debugging.

### Performance Consideration

Frequent API calls during typing may impact performance.
Implementing a **debounce mechanism** is recommended.

### Image Assets

Missing or incorrect icon paths may cause runtime errors. Ensure all referenced images exist.

---

# 🔮 Future Improvements

* Implement debounce for search input
* Improve user-friendly API error messages
* Cache API responses to reduce network usage
* Add multi-language support
* Support additional units (e.g., wind speed in mph)
* Improve accessibility (keyboard navigation, screen readers)

---

# 📜 License

This project is licensed under the **MIT License**.
See the `LICENSE` file for more details.

---

# 🙌 Acknowledgments

* OpenWeatherMap — Weather & geocoding services
* Open-Meteo — Forecast data
* OpenCage — Geolocation services
* PyQt5 — GUI framework

---
Developed as part of my Data Engineering learning journey.
