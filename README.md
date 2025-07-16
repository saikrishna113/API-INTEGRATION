COMPANY: CODTECH IT SOLUTIONS

NAME: Masagani sai krishna

INTERN ID: CT06DH1224

DOMAIN: Full Stack Web Development

DURATION: 6 WEEEKS

MENTOR:NEELA SANTOSH


# Weather Dashboard


A responsive web application that fetches and displays real-time weather data from public APIs. Built with vanilla HTML, CSS, and JavaScript.

## Features

- **Real-time Weather Data**: Fetches current weather information for any city
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Interactive Search**: Search by city name with Enter key support
- **Recent Searches**: Quick access to recently searched cities
- **Modern UI**: Glass-morphism design with smooth animations
- **Error Handling**: Graceful error messages and loading states
- **Multiple Cities**: Display weather for multiple cities simultaneously

## Demo

The current implementation uses mock data for demonstration purposes. To use real weather data, you'll need to integrate with a weather API service.

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- Optional: A web server for local development (Live Server, Python's http.server, etc.)

### Installation

1. Clone or download the project files
2. Open `index.html` in your web browser
3. Start searching for cities to see weather data

### Using Real Weather Data

To integrate with a real weather API:

1. **Sign up for a weather API service**:
   - [OpenWeatherMap](https://openweathermap.org/api) (Free tier available)
   - [WeatherAPI](https://www.weatherapi.com/) (Free tier available)
   - [AccuWeather](https://developer.accuweather.com/) (Free tier available)

2. **Get your API key** from the chosen service

3. **Update the JavaScript code**:
   ```javascript
   // Replace this in the script section
   const API_KEY = 'your-actual-api-key-here';
   const API_BASE_URL = 'https://api.openweathermap.org/data/2.5/weather';
   
   // Replace the generateMockWeatherData function with actual API call
   async function fetchWeatherData(cityName) {
       const response = await fetch(`${API_BASE_URL}?q=${cityName}&appid=${API_KEY}&units=metric`);
       const data = await response.json();
       // Handle the response data
   }
   ```

## Project Structure

```
weather-dashboard/
├── index.html          # Main HTML file with embedded CSS and JavaScript
├── README.md           # This file
└── assets/            # Optional: for additional resources
    ├── images/
    └── icons/
```

## Technologies Used

- **HTML5**: Semantic markup and structure
- **CSS3**: Modern styling with Grid, Flexbox, and animations
  - CSS Grid for responsive layout
  - Flexbox for component alignment
  - CSS Custom Properties (variables)
  - Backdrop-filter for glass-morphism effect
- **JavaScript (ES6+)**: Dynamic functionality
  - Async/await for API calls
  - DOM manipulation
  - Event handling
  - Local data management

## API Integration

### Current Implementation (Mock Data)

The current version generates mock weather data for demonstration:

```javascript
function generateMockWeatherData(cityName) {
    return {
        name: cityName,
        main: {
            temp: Math.floor(Math.random() * 30) + 5,
            feels_like: Math.floor(Math.random() * 30) + 5,
            humidity: Math.floor(Math.random() * 50) + 30,
            pressure: Math.floor(Math.random() * 50) + 1000
        },
        weather: [{
            main: randomCondition,
            description: randomCondition.toLowerCase()
        }],
        wind: {
            speed: Math.floor(Math.random() * 15) + 1
        }
    };
}
```

### Real API Integration Example

For OpenWeatherMap API:

```javascript
async function fetchWeatherData(cityName) {
    try {
        const response = await fetch(
            `${API_BASE_URL}?q=${cityName}&appid=${API_KEY}&units=metric`
        );
        
        if (!response.ok) {
            throw new Error(`HTTP error! status: ${response.status}`);
        }
        
        const data = await response.json();
        
        // Process and display the data
        weatherData.push(data);
        renderWeatherCards();
        
    } catch (error) {
        showError(`Error fetching weather for ${cityName}: ${error.message}`);
    }
}
```

## Features Explained

### Responsive Design
- Mobile-first approach
- CSS Grid for card layout
- Flexible typography scaling
- Touch-friendly interface

### Search Functionality
- Real-time search with Enter key support
- Input validation
- Recent searches tracking
- Quick re-search from history

### User Experience
- Loading states during API calls
- Error handling with user-friendly messages
- Smooth animations and transitions
- Intuitive interface design

## Browser Support

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## Performance Considerations

- Efficient DOM manipulation
- Minimal API calls (caching recent searches)
- Optimized CSS animations
- Responsive images and assets

## Security Notes

- Never expose API keys in client-side code for production
- Consider using environment variables or server-side proxy
- Implement rate limiting for API calls
- Validate and sanitize user input

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is open source and available under the [MIT License](LICENSE).

## Troubleshooting

### Common Issues

1. **API Key Errors**: Ensure your API key is valid and has the correct permissions
2. **CORS Errors**: Some APIs require server-side requests or CORS configuration
3. **Rate Limiting**: Implement proper request throttling for production use
4. **City Not Found**: Add better error handling for invalid city names

### Getting Help

- Check the browser console for error messages
- Verify API key and endpoint configuration
- Test with known working city names
- Ensure internet connectivity

## Future Enhancements

- [ ] Weather forecasts (5-day, hourly)
- [ ] Location-based weather detection
- [ ] Weather maps integration
- [ ] Favorite cities feature
- [ ] Weather alerts and notifications
- [ ] Dark/light theme toggle
- [ ] Export weather data
- [ ] Offline functionality with service workers

## Changelog

### Version 1.0.0
- Initial release with basic weather display
- Responsive design implementation
- Search functionality
- Recent searches feature
- Mock data integration

---

## OUTPUT:
<img width="1894" height="905" alt="Image" src="https://github.com/user-attachments/assets/b5738d34-3d7b-4410-a338-0c5ad3f771f4" />

<img width="1897" height="803" alt="Image" src="https://github.com/user-attachments/assets/bed871fd-9ca6-4a79-9adc-2b91a0ff7fdf" />
