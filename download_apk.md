# Expo EAS Build Commands for Android APK (PowerShell) to doanload the apk

## Step 1: Allow PowerShell script execution (run as Administrator)
```
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```
For a single time usage below command is much better 
```
 Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```
## Step 2: Login to Expo account (Will require login details and password)
```
eas login
```
## Step 3: Navigate to your project directory {The same directory from which you run the npx expo run command}
```
cd "C:\Users\ADMIN\Desktop\New folder\geotag_app"  #for example for my first app
```
## Step 4: Configure EAS for your project (only needed once)
```
eas build:configure
```
## Step 5: Build Android app (APK)
```
eas build -p android --profile preview
```

*Once the build is ready you can visit the expo cloud to see status and download the APK build from the mobile phone itself 

## Step 6: View build status
eas build:list

## Step 7: Download APK from Expo build dashboard
```
Visit: https://expo.dev/accounts/<your-username>/projects/<project-name>/builds
```
## Notes:
- Replace <your-username> and <project-name> in the URL.
- Use the same directory for all commands where your app.json and package.json are located.
