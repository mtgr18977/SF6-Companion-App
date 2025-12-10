# Street Fighter 6 Companion App

A mobile companion app for Street Fighter 6 players, providing quick access to frame data and character information. Built with Capacitor for cross-platform deployment on Android devices.

## Features

- **Comprehensive Frame Data**: Access detailed frame data for all Street Fighter 6 characters
- **Character Information**: Browse move lists with startup frames, active frames, recovery, and frame advantage data
- **Mobile-Optimized UI**: Vibrant, fighting game-inspired interface designed for mobile devices
- **Offline Access**: All frame data available without internet connection
- **Native Performance**: Built with Capacitor for smooth, native app experience

## Tech Stack

- **Framework**: Capacitor 8.0
- **Platform**: Android
- **Frontend**: HTML5, CSS3, JavaScript
- **Build Tools**: Gradle

## Project Structure

```
SF6-Companion-App/
├── www/                    # Web assets
│   ├── index.html         # Main app interface
│   └── sf6-frame-data.js  # Frame data for all characters
├── android/               # Android platform code
│   └── app/              # Android app module
├── resources/            # App resources (icons, splash screens)
├── capacitor.config.ts   # Capacitor configuration
└── package.json          # Node dependencies
```

## Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Android Studio (for Android development)
- Java Development Kit (JDK) 11 or higher

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/SF6-Companion-App.git
cd SF6-Companion-App
```

2. Install dependencies:
```bash
npm install
```

3. Sync Capacitor with the native project:
```bash
npx cap sync
```

## Development

### Running on Android

1. Open the Android project in Android Studio:
```bash
npx cap open android
```

2. Build and run the app from Android Studio, or use:
```bash
npx cap run android
```

### Making Changes

1. Edit files in the `www/` directory
2. Sync changes to the native project:
```bash
npx cap copy
```

## Building for Production

### Android APK

1. Open Android Studio:
```bash
npx cap open android
```

2. In Android Studio:
   - Select **Build** > **Build Bundle(s) / APK(s)** > **Build APK(s)**
   - The APK will be generated in `android/app/build/outputs/apk/`

### Android App Bundle (for Play Store)

```bash
cd android
./gradlew bundleRelease
```

The AAB file will be located at `android/app/build/outputs/bundle/release/`

## Frame Data

The app includes comprehensive frame data for all Street Fighter 6 characters, including:
- Startup frames
- Active frames
- Recovery frames
- Frame advantage on block
- Frame advantage on hit
- Special move properties and notes

## Configuration

The app is configured in `capacitor.config.ts`:
- **App ID**: `com.example.app`
- **App Name**: Street Fighter 6 Companion
- **Web Directory**: `www`

## License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

This is an unofficial fan-made companion app. Street Fighter and all related characters and assets are property of Capcom Co., Ltd. This app is not affiliated with, endorsed, or sponsored by Capcom.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Support

If you encounter any issues or have suggestions, please open an issue on GitHub.

---

**Note**: Frame data is subject to change with game updates and patches. Please verify critical information with official sources.
