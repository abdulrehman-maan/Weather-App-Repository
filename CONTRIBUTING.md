# Contributing to Weather App

Thank you for your interest in contributing to the Weather App! This document provides guidelines and information for contributors.

## 🤝 How to Contribute

### Reporting Issues
1. **Check existing issues** first to avoid duplicates
2. **Use the issue template** when creating new issues
3. **Provide detailed information** including:
   - Android version and device model
   - Steps to reproduce the issue
   - Expected vs actual behavior
   - Screenshots if applicable

### Suggesting Features
1. **Open a feature request** issue
2. **Describe the feature** in detail
3. **Explain the use case** and benefits
4. **Consider implementation complexity**

### Code Contributions

#### Prerequisites
- Android Studio (latest stable version)
- Java Development Kit (JDK) 8+
- Git knowledge
- Understanding of Android development

#### Development Setup
1. **Fork the repository**
   ```bash
   git clone https://github.com/yourusername/WeatherApp.git
   cd WeatherApp
   ```

2. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Open in Android Studio**
   - Import the project
   - Wait for Gradle sync
   - Ensure the app builds successfully

#### Coding Standards

##### Java Code Style
- **Indentation**: 4 spaces (no tabs)
- **Line length**: Maximum 120 characters
- **Naming conventions**:
  - Classes: `PascalCase` (e.g., `WeatherService`)
  - Methods: `camelCase` (e.g., `getCurrentWeather`)
  - Variables: `camelCase` (e.g., `weatherData`)
  - Constants: `UPPER_SNAKE_CASE` (e.g., `API_BASE_URL`)

##### Documentation
- **Add JavaDoc** for public methods and classes
- **Comment complex logic** inline
- **Update README** if adding new features

##### Example Code Style
```java
/**
 * Fetches current weather data for the specified city
 * @param cityName The name of the city
 * @return Weather object containing current conditions
 */
public Weather getCurrentWeather(String cityName) {
    // Validate input parameters
    if (cityName == null || cityName.trim().isEmpty()) {
        throw new IllegalArgumentException("City name cannot be null or empty");
    }
    
    // Implementation logic here
    return weatherData;
}
```

#### XML Layout Guidelines
- **Use meaningful IDs**: `@+id/textViewTemperature`
- **Follow Material Design**: Use Material components
- **Support different screen sizes**: Use responsive layouts
- **Add content descriptions**: For accessibility

#### Testing
- **Test on multiple devices** and screen sizes
- **Verify all weather conditions** display correctly
- **Test search functionality** with various inputs
- **Check orientation changes** work properly

#### Commit Guidelines
- **Use clear commit messages**:
  ```
  feat: Add 7-day weather forecast
  fix: Resolve temperature display issue
  docs: Update installation instructions
  style: Improve weather icon alignment
  ```

- **Keep commits focused**: One feature/fix per commit
- **Test before committing**: Ensure code builds and runs

#### Pull Request Process
1. **Update documentation** if needed
2. **Test thoroughly** on different devices
3. **Create pull request** with:
   - Clear title and description
   - Screenshots of UI changes
   - Testing information
   - Reference to related issues

4. **Respond to feedback** promptly
5. **Keep PR updated** with main branch

## 🎯 Areas for Contribution

### High Priority
- **Real API integration** (OpenWeatherMap, AccuWeather)
- **Location services** for GPS-based weather
- **Weather notifications** and alerts
- **Performance optimizations**

### Medium Priority
- **Additional weather details** (UV index, air quality)
- **Weather maps** integration
- **Dark mode** improvements
- **Accessibility** enhancements

### Low Priority
- **Weather widgets** for home screen
- **Multiple language** support
- **Weather animations** and transitions
- **Social sharing** features

## 🐛 Bug Reports

### Before Reporting
- **Update to latest version**
- **Check existing issues**
- **Try reproducing** on different devices

### Bug Report Template
```markdown
**Bug Description**
A clear description of the bug

**Steps to Reproduce**
1. Go to '...'
2. Click on '...'
3. See error

**Expected Behavior**
What should happen

**Actual Behavior**
What actually happens

**Environment**
- Device: [e.g. Samsung Galaxy S21]
- Android Version: [e.g. Android 12]
- App Version: [e.g. 1.0.0]

**Screenshots**
Add screenshots if applicable
```

## 🚀 Feature Requests

### Feature Request Template
```markdown
**Feature Description**
Clear description of the proposed feature

**Use Case**
Why is this feature needed?

**Proposed Solution**
How should this feature work?

**Alternatives Considered**
Other ways to solve this problem

**Additional Context**
Any other relevant information
```

## 📋 Code Review Process

### For Contributors
- **Be open to feedback**
- **Explain your approach** if complex
- **Update code** based on suggestions
- **Test changes** thoroughly

### For Reviewers
- **Be constructive** and helpful
- **Focus on code quality** and maintainability
- **Test the changes** if possible
- **Approve when ready**

## 🏆 Recognition

Contributors will be:
- **Listed in README** acknowledgments
- **Credited in release notes**
- **Invited to collaborate** on future features

## 📞 Getting Help

- **GitHub Issues**: For bugs and feature requests
- **Discussions**: For general questions
- **Code Comments**: For implementation details

## 📄 License

By contributing, you agree that your contributions will be licensed under the same MIT License that covers the project.

---

Thank you for contributing to Weather App! 🌤️