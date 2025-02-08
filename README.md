# Incorrect Dimensions from Dimensions.get('window') on Android

This repository demonstrates a bug in React Native where `Dimensions.get('window')` returns incorrect dimensions on Android, especially when launched from a notification or experiencing a delay. The provided solution shows how to reliably obtain accurate dimensions.

## Bug Description

The `Dimensions` API, commonly used for responsive design, can provide inaccurate window dimensions on Android under certain circumstances. This often results in UI elements being improperly positioned or sized. The inaccuracy becomes more pronounced when the application is launched from a background notification or after a short delay.

## Solution

The solution involves using the `Dimensions.addEventListener` method to listen for changes in the window dimensions. This method ensures that the application obtains the correct dimensions after they have stabilized.  The example shows how to set a state variable that updates on dimension changes and will have the correct dimensions after the initial calculation. 

## Setup and Run

1. Clone the repository.
2. Navigate to the repository directory.
3. Run `npm install` or `yarn install` to install the dependencies.
4. Run `npx react-native run-android` to start the app in Android emulator or device. 
5. Observe the initial dimensions (which may be incorrect) and how the app reacts as dimensions change.
