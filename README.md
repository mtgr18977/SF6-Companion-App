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

## Publishing to F-Droid

F-Droid is a catalog of FOSS (Free and Open Source Software) applications for Android. To submit your app:

### Prerequisites

1. **Make your app fully open source**: All code, assets, and dependencies must be FOSS-compatible
2. **Remove proprietary dependencies**: F-Droid only accepts apps that can be built entirely from source with FOSS tools
3. **Use a FOSS license**: Your LICENSE file should be GPL, Apache, MIT, or another FOSS-approved license

### Submission Process

1. **Prepare your repository**:
   - Ensure all source code is in a public Git repository (GitHub, GitLab, etc.)
   - Add proper version tags (e.g., `v1.0.0`, `v1.1.0`)
   - Include clear build instructions

2. **Create metadata**:
   - Fork the [F-Droid Data repository](https://gitlab.com/fdroid/fdroiddata)
   - Create a metadata file for your app in `metadata/com.example.app.yml`

3. **Metadata file example**:
```yaml
Categories:
  - Games
  - Sports
License: ISC
AuthorName: Your Name
AuthorEmail: your.email@example.com
SourceCode: https://github.com/yourusername/SF6-Companion-App
IssueTracker: https://github.com/yourusername/SF6-Companion-App/issues

AutoName: Street Fighter 6 Companion

RepoType: git
Repo: https://github.com/yourusername/SF6-Companion-App

Builds:
  - versionName: '1.0.0'
    versionCode: 1
    commit: v1.0.0
    subdir: android/app
    gradle:
      - yes

AutoUpdateMode: Version v%v
UpdateCheckMode: Tags
CurrentVersion: 1.0.0
CurrentVersionCode: 1
```

4. **Submit a merge request**:
   - Commit your metadata file to your forked repository
   - Create a merge request to the F-Droid Data repository
   - Include a clear description of your app

5. **Wait for review**:
   - F-Droid maintainers will review your submission
   - They may request changes or clarifications
   - The review process can take several weeks

### Important Considerations

- **Capcom Assets**: If your app uses Capcom's copyrighted assets (character images, logos, etc.), it may not be accepted by F-Droid due to licensing concerns
- **Frame Data**: Ensure frame data is either original research or properly licensed
- **Reproducible Builds**: F-Droid builds apps from source, so your build must be reproducible

### Alternative: F-Droid Repository

If your app doesn't meet F-Droid's strict requirements, you can create your own F-Droid repository:

1. Set up a simple repository with your APK files
2. Users can add your repository URL to their F-Droid client
3. Documentation: https://f-droid.org/docs/Setup_an_F-Droid_App_Repo/

### Useful Links

- [F-Droid Submission Guidelines](https://f-droid.org/docs/Inclusion_Policy/)
- [F-Droid Build Metadata Reference](https://f-droid.org/docs/Build_Metadata_Reference/)
- [F-Droid Data Repository](https://gitlab.com/fdroid/fdroiddata)

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
