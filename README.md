# AxoVids -> Android APK

The app is `www/index.html` (self-contained, works offline). Two ways to get an APK:

## A) Easiest: PWABuilder (no coding)
1. Host the `www` folder anywhere HTTPS (GitHub Pages / Netlify drop).
2. Go to pwabuilder.com, paste the URL, choose Android, download the package (APK/AAB).

## B) Capacitor (local build, needs Android Studio)
```
npm init -y
npm i @capacitor/core @capacitor/cli @capacitor/android
npx cap init AxoVids com.axolotking.axovids --web-dir=www
npx cap add android
npx cap sync
npx cap open android      # Build > Build APK(s) in Android Studio
```
Use `logo.svg` as the app icon (Android Studio: right-click res > New > Image Asset).
