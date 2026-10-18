# Website Specific Detox Lock (Keep Me Out Style)

This updated Android Studio project monitors mobile browsers and specifically triggers the phone lockdown ONLY when a specific targeted website (e.g., `facebook.com`, `instagram.com`, `youtube.com`) is opened in any mobile browser.

### How it Works:
1. **Target Website Input:** The user enters the specific website domain in `MainActivity` (e.g. `facebook.com`).
2. **Accessibility URL Inspection (`WebsiteAccessibilityService`):**
   - In real-time, it monitors browser address bars without battery drain.
   - When a browser URL contains the target domain, it immediately triggers the lockout.
3. **Immediate Screen Off & Lock:** Uses `DevicePolicyManager.lockNow()` to shut off the screen.
4. **Lockout Screen (`LockScreenActivity`):** Shows a full-screen lockout interface with countdown timer that prevents the user from accessing the browser.

### How to Build APK in Android Studio:
1. Unzip `BrowserLockApp_v2_Project.zip`.
2. Open Android Studio -> Click **Open** -> Select `BrowserLockApp_v2`.
3. Go to top menu: **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
4. Copy the generated `.apk` to your phone and install!
