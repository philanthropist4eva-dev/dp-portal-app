# DP Portal - Delivery Professionals Association Portal

A professional Android WebView application for the Delivery Professionals Association portal.

## Features

- ✅ WebView for seamless web app integration
- ✅ Pull-to-refresh functionality
- ✅ Loading progress indicator
- ✅ Offline error handling
- ✅ Back button navigation
- ✅ Smart link handling (internal/external)
- ✅ Camera and file upload support
- ✅ WhatsApp, phone, email, and maps integration
- ✅ JavaScript and DOM storage enabled
- ✅ Professional splash screen
- ✅ Production-ready for Google Play Store

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/philanthropist4eva-dev/dp-portal-app.git
cd dp-portal-app
```

### 2. Add App Icon
Replace `app/src/main/res/mipmap/ic_launcher.png` with `logo(10).png`

### 3. Add Splash Screens
Add splash screen images to `app/src/main/res/drawable/`:
- splash1.png
- splash2.png
- splash3.png

### 4. Configure Signing
Create `keystore.properties` in the project root:
```properties
storePassword=your_keystore_password
keyAlias=release_key
keyPassword=your_key_password
```

### 5. Build the App

#### Debug APK
```bash
./gradlew assembleDebug
```

#### Release APK
```bash
./gradlew assembleRelease
```

#### Release AAB (for Play Store)
```bash
./gradlew bundleRelease
```

## Project Structure

```
app/
├── src/main/
│   ├── java/com/deepee/association/
│   │   ├── MainActivity.kt         # Main WebView activity
│   │   └── SplashActivity.kt       # Splash screen
│   ├── res/
│   │   ├── layout/                 # XML layouts
│   │   ├── values/                 # Strings, colors, themes
│   │   ├── drawable/               # Icons and drawables
│   │   ├── mipmap/                 # App icons
│   │   └── xml/                    # Configuration files
│   └── AndroidManifest.xml
├── build.gradle.kts                # Module build configuration
└── proguard-rules.pro              # ProGuard configuration
```

## Configuration

### Package Name
- `com.deepee.association`

### Min/Target SDK
- Min SDK: 23 (Android 6.0)
- Target SDK: 34 (Android 14)

### Website URL
- `https://deepee.com.ng/association`

## Key Files

- **MainActivity.kt**: Core WebView implementation with all features
- **SplashActivity.kt**: Splash screen displayed on app launch
- **AndroidManifest.xml**: Permissions and app configuration
- **activity_main.xml**: Main layout with WebView, SwipeRefresh, and offline screen
- **activity_splash.xml**: Splash screen layout

## Security Features

- SSL pinning support
- Cleartext traffic disabled by default
- File provider for secure file access
- ProGuard code obfuscation enabled
- Resource shrinking enabled

## Permissions

- INTERNET (required)
- ACCESS_NETWORK_STATE (required)
- CAMERA (optional, for file upload)
- READ/WRITE_EXTERNAL_STORAGE (optional, for file access)

## Testing

1. Load the app on Android device/emulator
2. Test internal link navigation
3. Test external link handling (WhatsApp, phone, email, maps)
4. Test pull-to-refresh
5. Test offline handling by disabling internet
6. Test file upload and camera
7. Test back button navigation

## Google Play Store Publishing

1. Generate signed release AAB:
   ```bash
   ./gradlew bundleRelease
   ```

2. Upload `app/release/app-release.aab` to Play Console

3. Configure app details:
   - App name: DP Portal
   - Short description: Delivery Professionals Association Portal
   - Full description: [Add your description]
   - Screenshots: Add app screenshots
   - Icon: 512x512 PNG
   - Feature graphic: 1024x500 PNG

## Support

For issues or questions, contact: support@deepee.com.ng

## License

All rights reserved © Delivery Professionals Association
