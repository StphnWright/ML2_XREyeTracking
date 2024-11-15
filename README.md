# Magic Leap 2 Eye Tracking Interaction Project

This Unity project enables advanced eye-gaze interaction on Magic Leap 2, featuring customizable parameters for a target interactable sphere, as well as different modes for gaze-based interactions.

## Project Overview
- **Unity Version:** 2022.3.52f1  
- **Magic Leap SDK Version:** 2.5.0  
- **Magic Leap 2 OS Requirement:** Version 1.10.0 or later  
- **Scene for APK Build:** SampleScene  

---

## Setup Instructions

### Device Preparation
1. **Update Device OS:** Ensure that your Magic Leap 2 device is running OS version 1.10.0 or higher to support required features.
2. **Eye Tracking Calibration:** Calibrate eye tracking on the device before using the app. Detailed setup and calibration instructions can be found in the [Magic Leap 2 Documentation](https://developer-docs.magicleap.cloud/docs/guides/ml2-overview/).

### APK Installation and Debugging
1. **Install APK or Download Debug File:** Use Magic Leap Hub 3 to install the APK or access debug files. Download [Magic Leap Hub](https://ml2-developer.magicleap.com/downloads).
2. **Debug File Location:**  
   After running the app, the `debug_file.txt` file will be saved at:  
   `/storage/emulated/0/Android/data/com.ColumbiaCGUI.MagicLeap2EyeTracking/files/debug_file.txt`

---

## Application Overview
This version of the application provides interaction controls similar to the HoloLens version, allowing users to adjust parameters for a target interactable sphere in the scene.

---

## UI Controls

### Sliders
Configure the target interactable sphere:
- **R-radius:** Sets the radius of the target sphere.
- **X, Y, Z Position:** Sets the position of the target sphere along the respective axes.

### Toggles
- **Is Recording:** When enabled, records debug data for analysis.
- **Gaze Sphere:** Displays a cyan sphere representing gaze depth, calculated by a custom model, which is also used for interaction detection.
- **ML Gaze Sphere:** Displays a yellow sphere representing gaze depth as calculated by the Magic Leap SDK.
- **Ray Interaction:** Toggles interaction mode. When enabled, switches from sphere-collider interactions to raycasting, using the combined gaze position and direction directly from the Magic Leap SDK. In this mode, the custom model’s calculations do not influence interaction recognition, as combined gaze data from the SDK is used directly.
