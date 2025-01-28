# Expo CLI: Cryptic Errors Due to Version Mismatch

This repository demonstrates a common yet cryptic error in Expo CLI projects stemming from version mismatches between the Expo SDK, React Native, and third-party libraries. The issue manifests as seemingly nonsensical errors during build or runtime.

## Problem

The core issue is the use of library features or APIs that are not supported by the current Expo SDK or underlying React Native version. This incompatibility leads to errors such as `undefined is not an object (evaluating 'RNSensors.addListener')`, indicating a missing or incompatible module.

## Solution

The solution typically involves one or more of the following:

1. **Update Expo SDK:** Check for newer Expo SDK versions using `expo upgrade`. Often, the latest SDK fixes compatibility problems.
2. **Update React Native:** While less frequently directly controlled, ensuring that Expo's underlying React Native is up-to-date can solve compatibility issues.
3. **Review Library Compatibility:** Consult the documentation of any third-party libraries used. Ensure compatibility with your Expo SDK and React Native versions. Downgrading or upgrading the library might be necessary.
4. **Check Package.json:** Verify that all dependencies and peer dependencies are correctly specified and compatible.
5. **Clean and Rebuild:** Sometimes, a simple `expo start --clear` can resolve transient build issues.

This repository includes example code demonstrating a potential incompatibility and its resolution.