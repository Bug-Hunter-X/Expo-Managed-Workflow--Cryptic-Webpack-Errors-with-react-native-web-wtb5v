# Expo Managed Workflow: Cryptic Webpack Errors with react-native-web

This repository demonstrates a bug encountered in an Expo managed workflow project when using the `react-native-web` library and components that rely on specific Webpack features.  The Expo development server fails to start or provides unhelpful error messages.

## Bug Description

When using components with dynamic imports or loaders not directly supported by Expo's default Webpack setup, cryptic errors arise during the development server startup.  The problem stems from a conflict or incompatibility between the underlying Webpack configuration used by Expo and that needed by `react-native-web`.  Default Expo error messages aren't sufficient for debugging.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run `expo start`.
4. Observe the cryptic error messages during the development server startup.  Check the Webpack logs for detailed clues.

## Solution

The solution involves carefully analyzing Webpack logs and potentially customizing the Expo Webpack configuration (if possible within the managed workflow limitations). In some cases, refactoring components to avoid conflicting Webpack features might be necessary.  The `bugSolution.js` file provides a possible approach to resolve this, dependent on the specific component implementation and required webpack features.