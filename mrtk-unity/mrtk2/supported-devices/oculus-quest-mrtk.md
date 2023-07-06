---
title: Deploying to Quest
description: Documentation to configure for Quest in MRTK
author: RogPodge
ms.author: roliu
ms.date: 01/10/2023
keywords: Unity, HoloLens, HoloLens 2, Mixed Reality, development, MRTK, Oculus, Meta, Quest
---

# Deploying to Quest &#8212; MRTK2

A [Meta Quest (1 or 2)](https://www.meta.com/quest/products/quest-2/) is required.

## Setting up project for the Quest

1. Follow [these steps](https://developer.oculus.com/documentation/unity/book-unity-gsg/) to ensure that your project is ready to deploy on Quest.
1. Ensure that [developer mode](https://developer.oculus.com/documentation/native/android/mobile-device-setup/) is enabled on your device. Installing the Oculus ADB Drivers is optional.

## Setting up the scene

1. Create a new Unity scene or open a pre-existing scene like HandInteractionExamples.
    1. If creating a new scene, add MRTK to the scene by navigating to **Mixed Reality Toolkit** > **Add to Scene and Configure**.

## MRTK integration

[!INCLUDE[](includes/quest-deployment.md)]

## Build and deploy your project to Quest

1. Plug in your Quest via a USB 3.0 -> USB C cable
1. Navigate to **File > Build Settings**
1. Change the deployment to **Android**
1. Ensure that the Quest is selected as the applicable run device

    ![Quest Run Device](../images/cross-platform/oculus-quest/OculusRunDevice.png)

1. Select Build and Run
    - You may encounter the following set of build errors when you select *Build and Run* the first time. It shouldn't prevent deployment. See [issue #10449](https://github.com/microsoft/MixedRealityToolkit-Unity/issues/10449#issuecomment-1370174718) for more information and potential mitigation options.

    ![Quest Expected Build Errors](../images/cross-platform/oculus-quest/OculusExpectedBuildErrors.png)

1. Accept the *Allow USB Debugging* prompt from inside the Quest
1. See your scene inside the Quest

## Common errors

### Quest not recognized by Unity

Make sure your Android paths are properly configured. If you continue to encounter problems, follow this [guide](https://developer.oculus.com/documentation/unity/book-unity-gsg/#install-android-tools).

Look under **Edit > Preferences > External Tools > Android**:

![Android Tools Config](../images/cross-platform/oculus-quest/AndroidToolsConfig.png)
