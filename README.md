# 🌤️ Weather Explorer

A simple, responsive weather web app that shows current conditions and a 4-day forecast for any city, powered by the [OpenWeatherMap API](https://openweathermap.org/api).

## Features

- 🔍 Search current weather by city name
- 🌡️ Displays temperature, description, and weather icon
- 📅 4-day forecast with daily temperature and icons
- 🎨 Clean, dark-themed responsive UI

## Demo

Simply open `index.html` in your browser — no build step required.

## Project Structure

```
weather-explorer/
├── index.html      # App markup
├── styles.css       # Styling and layout
├── script.js         # Weather fetching logic
└── README.md
```

## Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/weather-explorer.git
   cd weather-explorer
   ```

2. **Get an API key**
   Sign up for a free API key at [OpenWeatherMap](https://home.openweathermap.org/users/sign_up).

3. **Add your API key**
   Open `script.js` and replace the placeholder with your own key:
   ```js
   const apiKey = 'YOUR_API_KEY_HERE';
   ```

   > ⚠️ **Security note:** Never commit a real API key to a public repository. Consider using an environment variable, a config file excluded via `.gitignore`, or a backend proxy to keep your key private.

4. **Open the app**
   Just open `index.html` in your browser, or serve it locally:
   ```bash
   npx serve .
   ```

## How It Works

- Enter a city name and click **Search**.
- The app calls OpenWeatherMap's `/weather` endpoint for current conditions and `/forecast` endpoint for the 5-day/3-hour forecast, sampling one reading per day.
- Weather icons are pulled directly from OpenWeatherMap's icon CDN.

## Roadmap / Ideas

- [ ] Dynamically change background based on weather condition (`changeBackground()` is defined but not yet wired to live data)
- [ ] Add loading and error states in the UI (currently errors only log to console)
- [ ] Support geolocation-based weather lookup
- [ ] Add unit toggle (°C / °F)

## License

This project is open source and available under the [MIT License](LICENSE).
