# MaestroDev – Mobile UI Testing with Maestro


Automated mobile UI tests for Android using MaestroDev

This project shows how to set up Maestro, run flows against an Android emulator, and install a sample APK to test.



## 💻 Prerequisites

1. Java 11+ (JDK).

2. Android SDK (installed with Android Studio or command-line tools).

3. ADB in your PATH (platform-tools).

4. macOS / Linux / Windows



## 🚀 Install Maestro

```bash
curl -Ls "https://get.maestro.mobile.dev" | bash
maestro --version
```

##  🤖 Android setup (SDK, Emulator, ADB)


1. Install Android Studio (includes SDK Manager & AVD Manager).

2. Install Platform Tools (ADB) and at least one Android System Image

## 📱 Create an emulator in Android Studio (GUI)

1. Open Android Studio → More Actions → AVD Manager.

2. Create Virtual Device… → Choose a device (e.g., Pixel 6).

3. Pick a System Image (e.g., API 34/35).

4. Finish and Start the emulator.

Verify with:
```bash
adb devices
```

## 💾 Install the sample APK

1. Get Mestro dev.


```bash
curl -Ls "https://get.maestro.dev" | bash
```


2. Download official sample.

```bash
maestro download-samples
```


3. Install APK sample in the emulator.

```bash
cd samples
adb install sample.apk
```

##  📂  Project structure
```bash
MaestroDev/
├─ tests/ 
│  ├─ sample_login.yaml
│  └─ wikipedia/change_theme.yaml
├─ samples/
│  └─ wikipedia.apk
├─ README.md
└─ .gitignore
```
## 📘 How to run the tests


Make sure the emulator is running and visible to ADB:


```bash
adb devices
```
Run a single flow

```bash
adb maestro test tests/scrollTillText.yaml
```

## 👤 Author
Nicolás Carlos Maranesi

QA Automation Engineer / Test Architect

LinkedIn: nicolas-maranesi