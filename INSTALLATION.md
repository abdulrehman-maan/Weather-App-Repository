# 📱 Installation Guide

Complete guide for setting up and running the Weather App on your development environment.

## 🔧 Prerequisites

### Required Software
- **Android Studio**: Arctic Fox (2020.3.1) or later
- **Java Development Kit (JDK)**: Version 8 or higher
- **Android SDK**: API level 21 (Android 5.0) or higher
- **Git**: For version control

### System Requirements
- **Operating System**: Windows 10+, macOS 10.14+, or Linux (Ubuntu 18.04+)
- **RAM**: Minimum 8GB (16GB recommended)
- **Storage**: At least 4GB free space
- **Internet Connection**: For downloading dependencies

## 📥 Download and Setup

### Method 1: Clone from GitHub

1. **Open Terminal/Command Prompt**
   ```bash
   cd /path/to/your/projects
   ```

2. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/WeatherApp.git
   cd WeatherApp
   ```

3. **Verify Files**
   ```bash
   ls -la
   # Should show: app/, build.gradle.kts, settings.gradle.kts, etc.
   ```

### Method 2: Download ZIP

1. **Download ZIP file** from GitHub
2. **Extract** to your desired location
3. **Rename folder** to `WeatherApp` (if needed)

## 🛠️ Android Studio Setup

### 1. Open Project

1. **Launch Android Studio**
2. **Select**: `File > Open`
3. **Navigate** to the `WeatherApp` folder
4. **Click**: `OK`

### 2. Gradle Sync

1. **Wait for automatic sync** (may take 2-5 minutes)
2. **If sync fails**:
   - Click `Sync Now` in the notification bar
   - Check internet connection
   - Verify JDK version in `File > Project Structure`

### 3. SDK Configuration

1. **Open SDK Manager**: `Tools > SDK Manager`
2. **Ensure installed**:
   - Android SDK Platform 34 (Android 14)
   - Android SDK Platform 21 (Android 5.0)
   - Android SDK Build-Tools 34.0.0
   - Google Play Services

### 4. AVD Setup (Optional)

1. **Open AVD Manager**: `Tools > AVD Manager`
2. **Create Virtual Device**:
   - Choose device (e.g., Pixel 4)
   - Select system image (API 21+ recommended)
   - Configure settings
   - Click `Finish`

## 📱 Running the App

### On Emulator

1. **Start AVD**: Click play button in AVD Manager
2. **Wait for boot**: Emulator should show home screen
3. **Run app**: Click green play button (▶️) in Android Studio
4. **Select target**: Choose your emulator
5. **Install and launch**: App will build and install automatically

### On Physical Device

1. **Enable Developer Options**:
   - Go to `Settings > About Phone`
   - Tap `Build Number` 7 times
   - Go back to `Settings > Developer Options`

2. **Enable USB Debugging**:
   - In Developer Options, enable `USB Debugging`
   - Connect device via USB
   - Allow debugging when prompted

3. **Run app**: Click green play button (▶️) in Android Studio
4. **Select device**: Choose your connected device
5. **Install**: App will build and install

## 🔍 Troubleshooting

### Common Issues

#### Gradle Sync Failed
```bash
# Solution 1: Clean and rebuild
./gradlew clean
./gradlew build

# Solution 2: Invalidate caches
# File > Invalidate Caches and Restart
```

#### SDK Not Found
1. **Check SDK path**: `File > Project Structure > SDK Location`
2. **Download missing components**: `Tools > SDK Manager`
3. **Update local.properties**:
   ```properties
   sdk.dir=/path/to/your/Android/Sdk
   ```

#### Build Errors
```bash
# Check Java version
java -version

# Should be Java 8 or higher
# Update JDK if needed
```

#### App Won't Install
1. **Check device compatibility**: API 21+ required
2. **Enable unknown sources**: For sideloading
3. **Clear app data**: If previous version exists
4. **Restart device**: Sometimes helps with installation issues

### Performance Issues

#### Slow Build Times
1. **Increase heap size**: Add to `gradle.properties`
   ```properties
   org.gradle.jvmargs=-Xmx4g -XX:MaxPermSize=512m
   org.gradle.parallel=true
   org.gradle.daemon=true
   ```

2. **Enable offline mode**: `File > Settings > Build > Gradle`
3. **Use latest Gradle**: Check `gradle/wrapper/gradle-wrapper.properties`

#### Emulator Performance
1. **Enable hardware acceleration**: Intel HAXM or AMD Hypervisor
2. **Allocate more RAM**: In AVD settings
3. **Use x86 images**: Instead of ARM for better performance

## 📋 Verification

### Test Installation

1. **App launches successfully**
2. **Main screen shows weather data**
3. **Search functionality works**
4. **Forecast displays correctly**
5. **No crash or error messages**

### Test Features

- [ ] **Current weather display**
- [ ] **5-day forecast**
- [ ] **City search**
- [ ] **Pull to refresh**
- [ ] **Orientation changes**
- [ ] **Different weather conditions**

## 🔧 Development Setup

### Code Style

1. **Import code style**: `File > Settings > Editor > Code Style`
2. **Use project settings**: Should be automatic
3. **Format code**: `Ctrl+Alt+L` (Windows/Linux) or `Cmd+Alt+L` (Mac)

### Git Configuration

```bash
# Set up Git (if not already done)
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Create feature branch
git checkout -b feature/your-feature-name
```

### Debugging

1. **Set breakpoints**: Click left margin in code editor
2. **Debug mode**: Click debug button (🐛) instead of run
3. **Use logcat**: `View > Tool Windows > Logcat`

## 📚 Next Steps

### After Installation

1. **Read the README**: Understand app features and architecture
2. **Explore the code**: Start with `MainActivity.java`
3. **Run tests**: Verify everything works correctly
4. **Make changes**: Try modifying weather data or UI
5. **Contribute**: See `CONTRIBUTING.md` for guidelines

### Learning Resources

- [Android Developer Docs](https://developer.android.com/)
- [Material Design Guidelines](https://material.io/design)
- [Java Documentation](https://docs.oracle.com/javase/8/docs/)
- [Git Tutorial](https://git-scm.com/docs/gittutorial)

## 📞 Support

If you encounter issues:

1. **Check this guide** for common solutions
2. **Search existing issues** on GitHub
3. **Create new issue** with detailed information
4. **Include**:
   - Android Studio version
   - Java version
   - Device/emulator details
   - Error messages
   - Steps to reproduce

---

Happy coding! 🌤️👨‍💻