---
title: Build and deploy to the HoloLens
description: This article outlines building your mixed reality project with Unity and Visual Studio so you can deploy it to the HoloLens.
author: mattzmsft
ms.author: vinnietieto
ms.date: 9/6/2022
ms.topic: article
keywords: unity, visual studio, export, build, deploy, HoloLens, mixed reality headset, windows mixed reality headset, virtual reality headset, UWP, deploying
---

# Build and deploy to the HoloLens

Before you build and deploy your project, make sure that you have already [set up your XR configuration and switched to the Universal Windows Platform](choosing-unity-version.md).

## Build the Unity project

1. In Unity on the menu bar, select **File** > **Build Settings...**.
1. In the **Build Settings** window, select the **Add Open Scenes** button. This adds your current scene to the **Scenes In Build** list.

    ![Screen shot of Unity build settings](images/023-build-settings.png)

1. If you followed the instructions in the [Set up a new OpenXR project with MRTK](new-openxr-project-with-mrtk.md) article, you should have all the correct settings for a Universal Windows Platform build in place. As a reminder, here are the important settings once again:

    -Set **Build Type** to *D3D Project*  
    -Set **Target SDK Version** to *Latest installed*  
    -Set **Minimum Platform Version** to *10.0.10240.0*  
    -Set **Visual Studio Version** to *Latest installed*

    Feel free to leave other settings not covered above to the default, as for example some only apply to the **Build And Run** option. Please refer to [Unity's documentation](https://docs.unity3d.com/Manual/windowsstore-buildsettings.html) for more information on the other settings.

1. Click the **Build** button.
1. In the **Build Universal Windows Platform** dialog, choose the folder you want to store your build in. (To keep things organized, you may want to create a folder named **Builds**, or something similar, and then save your build there.) 
1. Select the folder you chose and then click **Select Folder** to start the build process.

## Building and deploying a Unity Visual Studio solution

1. After Unity has finished building the project, a Windows Explorer window will open to the project root directory. Navigate into the folder that contains your newly-created solution file.
1. Find the solution file located inside this folder and open it.

The remainder of building and deploying apps happens in [Visual Studio](../advanced-concepts/using-visual-studio.md).

## Rebuilding your project

If you make changes to your project, you'll need to do another build from Unity. Some examples of changes are:
* You change a script.
* You add or remove assets in the Project tab.
* You change any value in the Inspector tab.
* You add or remove objects from the Hierarchy tab.
* You change any Unity project settings.