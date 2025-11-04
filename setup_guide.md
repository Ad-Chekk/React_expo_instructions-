React Expo Android App Setup Guide
====================================

1. Basic Requirements
---------------------
- Install Node.js (LTS) from https://nodejs.org
  Check versions:
  ```
    node -v
    npm -v
  ```
- Install Git
- ```
    git --version
  ```
- Install Java JDK 17+ (from https://adoptium.net/)
- Install Expo CLI globally:
- ```
    npm install -g expo-cli
  ```

2. Create a New Expo Project
----------------------------
Use the latest Expo SDK:
```
    npx create-expo-app myApp
    cd myApp
```

(Optional) Choose template:
- blank
- blank (TypeScript)
- tabs

3. Install Dependencies
-----------------------
Install base dependencies:
```
    npm install
```
Common packages:
- Navigation:
    npm install @react-navigation/native
    npx expo install react-native-screens react-native-safe-area-context
    npm install @react-navigation/native-stack
- Icons:
    npx expo install @expo/vector-icons
- Permissions:
    npx expo install expo-permissions
- Camera & Media:
    npx expo install expo-camera expo-media-library
- File System:
    npx expo install expo-file-system
- Image Picker:
    npx expo install expo-image-picker
- Async Storage:
    npx expo install @react-native-async-storage/async-storage
- Axios for API calls:
    npm install axios

4. Run on Expo Go App
---------------------
- Install Expo Go from Play Store.
- Run this command from the project directory ie "myApp"
  ```
    npx expo start
  ```
- Scan the QR code from terminal using Expo Go app.

5. Typical Project Structure
----------------------------
myApp/
├── App.js
├── package.json
├── app.json
├── assets/
│   └── icon.png
│   └── splash.png
├── components/
│   └── CustomButton.js
├── screens/
│   └── HomeScreen.js
│   └── SettingsScreen.js
└── utils/
    └── api.js

6. Developer Tools
------------------
- VS Code (recommended)
- ESLint + Prettier for code formatting
Install linting tools:
    npm install --save-dev eslint prettier eslint-config-prettier eslint-plugin-prettier

7. Environment Variables
------------------------
Create a .env file for API keys:
    API_URL=https://api.example.com
Install dotenv:
    npm install react-native-dotenv
Import in code:
    import { API_URL } from "@env";

8. Build Android APK / AAB
---------------------------
Login to Expo:
```
    npx expo login
```
Build command:
```
    npx expo build:android
```
or with new EAS build system:
```
    npx expo prebuild
    npx expo run:android
```
or
```
    npx eas build -p android --profile preview
```

9. Optional Enhancements
------------------------
- State management: Zustand / Redux Toolkit
- Styling: NativeWind (Tailwind for RN)
- Animations: React Native Reanimated / Moti
- Notifications: expo-notifications
- Storage: expo-sqlite / expo-secure-store

10. Clean Run Checklist
-----------------------
✅ Node & Expo installed
✅ Project created via 'npx create-expo-app'
✅ Dependencies installed via 'npx expo install'
✅ Expo Go installed on Android
✅ Project runs via 'npx expo start'
✅ QR code scanned successfully

End of Instructions
====================================
