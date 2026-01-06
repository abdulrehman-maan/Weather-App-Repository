# Weather App - Complete Android Application

A beautiful, feature-rich Android weather application that displays current weather conditions and 5-day forecasts. Built with Java and modern Android development practices.

## 🌟 Features

### ✅ **Current Weather Display**
- Real-time weather information
- Temperature with "feels like" indicator
- Weather condition descriptions
- Beautiful weather-specific backgrounds
- Location-based weather data

### ✅ **Detailed Weather Information**
- **Humidity** - Current humidity percentage
- **Wind Speed** - Wind speed in km/h
- **Pressure** - Atmospheric pressure in hPa
- **Visibility** - Visibility distance in km
- **Sunrise/Sunset** - Daily sun times

### ✅ **5-Day Weather Forecast**
- Horizontal scrollable forecast cards
- Daily high/low temperatures
- Weather condition icons
- Humidity and wind information
- Rain chance indicators

### ✅ **City Search & Selection**
- Search from 100+ popular cities worldwide
- Real-time search filtering
- Easy city selection interface
- Instant weather updates

### ✅ **Beautiful User Interface**
- **Material Design 3** components
- **Dynamic backgrounds** that change with weather conditions
- **Weather-specific icons** for all conditions
- **Smooth animations** and transitions
- **Responsive design** for all screen sizes

### ✅ **User Experience Features**
- **Pull-to-refresh** functionality
- **Swipe gestures** for easy navigation
- **Loading indicators** for better feedback
- **Error handling** with user-friendly messages
- **Offline-ready** with mock data for demo

## 🏗️ Technical Architecture

### **Technology Stack**
- **Language**: Java (100% Java, no Kotlin)
- **Platform**: Android (API 21+)
- **Architecture**: Clean Architecture with separation of concerns
- **UI Framework**: Material Design 3
- **Data**: Mock weather service (easily replaceable with real API)

### **Key Components**
- **MainActivity**: Main weather display with current conditions and forecast
- **SearchActivity**: City search and selection interface
- **WeatherService**: Weather data fetching and processing
- **ForecastAdapter**: RecyclerView adapter for forecast display
- **WeatherIconUtils**: Weather icon and background management

### **Design Patterns Used**
- **Adapter Pattern**: For RecyclerView forecast display
- **Factory Pattern**: For weather icon selection
- **Observer Pattern**: For UI updates via callbacks
- **Singleton Pattern**: For weather service management

## 📱 Screenshots & UI

### **Main Weather Screen**
- Large temperature display
- Weather condition icon
- Current date and location
- Detailed weather metrics in cards
- Horizontal forecast scroll

### **Search Interface**
- Clean search input
- Filtered city list
- Instant search results
- Easy city selection

### **Dynamic Backgrounds**
- **Sunny**: Warm orange/yellow gradients
- **Cloudy**: Cool blue/gray gradients
- **Rainy**: Deep blue gradients
- **Night**: Dark purple/blue gradients
- **Stormy**: Dark gray/black gradients

## 🚀 How to Run

### **Prerequisites**
- Android Studio (Latest stable version)
- Java Development Kit (JDK) 8+
- Android SDK (API 21+)

### **Installation Steps**
1. **Open Android Studio**
2. **Import Project**: File → Open → Select `WeatherApp` folder
3. **Sync Project**: Wait for Gradle sync to complete
4. **Run App**: Click green play button (▶️)

### **Device Requirements**
- **Minimum SDK**: API 21 (Android 5.0)
- **Target SDK**: API 34 (Android 14)
- **Permissions**: Internet access (for future API integration)

## 🎯 App Usage

### **Getting Weather Information**
1. **Launch app** - Shows default city weather (London)
2. **View current conditions** - Temperature, description, details
3. **Check forecast** - Scroll through 5-day forecast cards
4. **Refresh data** - Pull down to refresh or use menu

### **Searching Cities**
1. **Tap search icon** in toolbar
2. **Type city name** in search box
3. **Select city** from filtered results
4. **View weather** - Automatically loads new city weather

### **Weather Details**
- **Current Temperature**: Large display with feels-like temperature
- **Weather Condition**: Icon and description
- **Detailed Metrics**: Humidity, wind, pressure, visibility, sunrise/sunset
- **5-Day Forecast**: Daily highs/lows with conditions

## 🔧 Customization & Extension

### **Adding Real Weather API**
The app uses mock data for demo purposes. To integrate a real weather API:

1. **Get API Key** from OpenWeatherMap or similar service
2. **Update WeatherService.java**:
   ```java
   // Replace mock data methods with real API calls
   private static final String API_KEY = "your_api_key_here";
   ```
3. **Uncomment API code** in `WeatherService.java`
4. **Add network permissions** (already included)

### **Adding New Cities**
Edit `SearchActivity.java` and add cities to the `popularCities` array:
```java
private String[] popularCities = {
    "Your City, Country",
    // ... existing cities
};
```

### **Customizing Weather Icons**
Add new weather icons in `res/drawable/` and update `WeatherIconUtils.java`:
```java
case "new_condition":
    return R.drawable.ic_weather_new_condition;
```

### **Adding New Weather Details**
1. Add new fields to `Weather.java` model
2. Update `WeatherService.java` to populate data
3. Add UI elements to `activity_main.xml`
4. Update `MainActivity.java` to display new data

## 📊 Weather Data Structure

### **Current Weather Model**
```java
public class Weather {
    private String cityName;
    private String country;
    private double temperature;
    private String description;
    private String weatherIcon;
    private int humidity;
    private double windSpeed;
    private double feelsLike;
    private int pressure;
    private int visibility;
    private String sunrise;
    private String sunset;
}
```

### **Forecast Model**
```java
public class Forecast {
    private String date;
    private String dayName;
    private double maxTemp;
    private double minTemp;
    private String description;
    private String weatherIcon;
    private int humidity;
    private double windSpeed;
    private int chanceOfRain;
}
```

## 🎨 Design System

### **Color Palette**
- **Primary**: Blue (#2196F3)
- **Accent**: Orange (#FF9800)
- **Background**: White/Light Gray
- **Text**: Dark Gray (#212121)

### **Weather-Specific Colors**
- **Sun**: Golden Yellow (#FFD54F)
- **Clouds**: Blue Gray (#90A4AE)
- **Rain**: Blue (#42A5F5)
- **Snow**: Light Blue (#E3F2FD)
- **Storm**: Dark Gray (#455A64)

### **Typography**
- **Temperature**: 64sp, Bold
- **City Name**: 24sp, Bold
- **Details**: 16sp, Regular
- **Forecast**: 14sp, Regular

## 🔍 Testing

### **Manual Testing Checklist**
- [ ] App launches successfully
- [ ] Current weather displays correctly
- [ ] Weather details show proper values
- [ ] 5-day forecast loads and scrolls
- [ ] Search functionality works
- [ ] City selection updates weather
- [ ] Pull-to-refresh works
- [ ] Background changes with weather conditions
- [ ] All weather icons display correctly

### **Test Cities**
Try these cities to see different weather conditions:
- **London** - Default city
- **Dubai** - Hot/sunny conditions
- **Seattle** - Rainy conditions
- **Moscow** - Cold/snowy conditions
- **Mumbai** - Humid conditions

## 🚀 Future Enhancements

### **Planned Features**
- **Location Services**: GPS-based weather
- **Weather Alerts**: Severe weather notifications
- **Multiple Locations**: Save favorite cities
- **Weather Maps**: Radar and satellite imagery
- **Widgets**: Home screen weather widgets
- **Dark Mode**: Enhanced dark theme support

### **Technical Improvements**
- **Real API Integration**: OpenWeatherMap API
- **Caching**: Offline weather data storage
- **Background Updates**: Periodic weather refresh
- **Push Notifications**: Weather alerts
- **Analytics**: Usage tracking and insights

## 📄 License

This project is created for educational and demonstration purposes. Feel free to use, modify, and distribute as needed.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📞 Support

For questions, issues, or suggestions:
- Check the code comments for implementation details
- Review the README for usage instructions
- Test with different cities and weather conditions

---

**🌤️ Weather App - Beautiful Weather, Beautiful Code**

*Built with ❤️ using Java and Android Studio*