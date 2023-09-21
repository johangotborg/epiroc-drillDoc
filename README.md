# Epiroc-drillDoc
Part of the IMMINENCE project, in collaboration with Epiroc and RISE. An application for fault classification in drill heads.

## Project Overview
This application has been designed for technicians working on 
drill sites. The main purpose of the app is to facilitate the "Add 
Task Process", which allows technicians to scan an RFID tag on the 
drill, upload images of the drill head to the AI algorithm on the 
backend, and submit the task details.

### Missing/Inconsistent Functionality and Proposed Changes
* The RFID functionality has been partially implemented, but the app currently fails to detect the RFID scanner and cannot read tags. To enable testing and demonstration of multiple tasks, the app utilizes mock data with randomized IDs.
* Currently, there is no access to the drill data database. Instead, the app relies on mock data for testing purposes.
* Missing API endpoint required for the integration of the ML algorithm 
* The app should connect to the front edge camera, as the RFID scanner blocks the back camera.
* Users are unable to abort a task process. This functionality needs to be added to ensure a coherent user experience.
* Task display: Users are currently able to view and delete all tasks on their home screen, including tasks submitted by other users. Proposed change: Users are able to view their own tasks on the home screen, but able to search for other tasks. Users can only delete/modify their own tasks.
* There are design inconsistencies between the login and register views and the rest of the app's UI. This issue should be addressed to provide a cohesive user experience.
* The app exhibits inconsistent behavior when the device is not connected to the internet. This issue should be addressed and resolved to ensure more robust functionality regardless of the network status.
* Ability to export task details to PDF.

### File Structure
- `android/`: Contains the Android-specific files and directories, including build files.
- `src/`: Contains the application source code.
    - `components/`: Contains reusable UI components.
    - `images/`: Contains static assets, such as images.
    - `models/`: Contains the data model classes.
    - `presenters/`: Contains the presenter classes.
    - `routers/`: Contains navigation-related files.
    - `store/`: Contains files related to state management.
    - `utilities/`: Contains utility functions.
    - `views/`: Contains the screen components.
    - `App.js`: The main entry point for the app.
    - `index.js`: The initializer for React Native.
- `Gemfile`: The Ruby dependencies file.
- `app.json`: Contains the configuration for the app.
- `package-lock.json`: The lock file for the npm dependencies.
- `package.json`: The npm dependencies file.


## Testing and Review
Link to app: https://appdistribution.firebase.dev/i/568532123ca88523

1. Log in to your Google account on your **Android device**
2. Click the link above
3. Enable installations from unknown sources
4. Use Firebase App Distribution to download DrillDoc
5. Start testing!

## Installation
- Clone repository
- run <code>npm install</code>
- run <code>npx react-native start</code> in project folder, then press <code>a</code> to launch application inside emulator

## Dependencies
    "@babel/preset-react": "^7.22.3",
    "@google-cloud/storage": "^6.10.1",
    "@react-native-async-storage/async-storage": "^1.18.1",
    "@react-navigation/drawer": "^6.6.2",
    "@react-navigation/native": "^6.1.6",
    "@react-navigation/native-stack": "^6.9.12",
    "@reduxjs/toolkit": "^1.9.3",
    "color-convert": "^2.0.1",
    "firebase": "^9.19.1",
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "react-native": "^0.71.4",
    "react-native-camera": "^4.2.1",
    "react-native-crypto": "^2.2.0",
    "react-native-elements": "^3.4.3",
    "react-native-gesture-handler": "^2.9.0",
    "react-native-keyboard-aware-scroll-view": "^0.9.5",
    "react-native-linear-gradient": "^2.6.2",
    "react-native-reanimated": "^2.14.4",
    "react-native-safe-area-context": "^4.5.0",
    "react-native-screens": "^3.20.0",
    "react-native-vector-icons": "^9.2.0",
    "react-native-vision-camera": "^2.15.4",
    "react-redux": "^8.0.5",
    "react-router-dom": "^6.8.2",
    "react-router-native": "^6.8.2",
    "redux": "^4.2.1",
    "redux-thunk": "^2.4.2"
    "@babel/core": "^7.20.0",
    "@babel/preset-env": "^7.20.0",
    "@babel/runtime": "^7.22.3",
    "@react-native-community/eslint-config": "^3.2.0",
    "@tsconfig/react-native": "^2.0.2",
    "@types/jest": "^29.2.1",
    "@types/react": "^18.0.24",
    "@types/react-test-renderer": "^18.0.0",
    "babel-jest": "^29.2.1",
    "eslint": "^8.19.0",
    "jest": "^29.2.1",
    "metro-react-native-babel-preset": "0.73.8",
    "prettier": "^2.4.1",
    "react-test-renderer": "18.2.0",
    "typescript": "4.8.4"
 

