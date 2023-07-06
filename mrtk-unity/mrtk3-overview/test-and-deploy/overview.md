---
title: Test and Experience Overview
description: Overview of how to test and experience your application on a device.
author: RogPodge
ms.author: roliu
ms.date: 1/13/2023
ms.localizationpriority: high
keywords: Unity, HoloLens, HoloLens 2, Mixed Reality, development, MRTK3, overview, setup, deployment, remoting, new project, getting started, tutorial, introduction, intro
---

# Testing and experiencing overview

Now that you have a Unity project with MRTK3, there are several means to test and experience your application.

## Preview your application

Compiling and deploying your app can take a significant amount of time, so we recommend using the following instant iteration/preview solutions while developing your application.

- [In-editor input simulation](../../mrtk3-input/packages/input/input-simulation.md)
    - Easily preview your app without any XR device attached. Control the user's head, hands, and hand gestures with traditional WASD controls.

- [Stream to a device](streaming.md)
    - These solutions allow you to run the app locally in the Unity editor in Play Mode and stream the experience to your device. All inputs from your device are sent to the PC, where the content is then rendered in a virtual immersive view. We highly recommend this solution for instant iteration and for showcasing prototypes

## Build and deploy

The following guides will walk you through building and running your application on a device.

- [HoloLens2](hololens2-deployment.md)
- [Quest Devices](quest-deployment.md)

If you've deployed a build to your target device of choice, you can debug the build as it runs on device with [Managed debugging](/windows/mixed-reality/develop/unity/managed-debugging-with-unity-il2cpp).
