---
title: Set up a new OpenXR project with MRTK
description: How to set up a new OpenXR project with MRTK.
author: sean-kerawala
ms.author: vinnietieto
ms.date: 04/12/2022
ms.topic: article
keywords: mixedrealitytoolkit, mixedrealitytoolkit-unity, mixed reality headset, windows mixed reality headset, virtual reality headset, unity, MRTK, unity
---

# Set up a new OpenXR project with MRTK

The easiest way to get your Unity project set up for mixed reality is with the [Mixed Reality Toolkit (MRTK)](/windows/mixed-reality/mrtk-unity). MRTK for Unity is an open-source, cross-platform development kit designed to make it easy to build amazing mixed reality applications.

   :::image type="content" source="images/MRTK_UX_Hero.png" alt-text="Infographic showing some of the features of the Mixed Reality Toolkit.":::

MRTK provides a cross-platform input system, foundational components, and common building blocks for spatial interactions. It can help you speed up your application development for Microsoft HoloLens, Windows Mixed Reality immersive (VR) headsets, and many other VR/AR devices. The project is aimed at reducing barriers to entry, enabling everyone to build mixed reality applications and contribute back to the community as we all grow.

MRTK supports a wide range of platforms, including:

- Microsoft HoloLens

- Microsoft HoloLens 2

- Windows Mixed Reality headsets

- OpenVR headsets (HTC Vive / Oculus Rift)

- Ultraleap Hand Tracking

- Android and iOS devices

> [!NOTE]
> You can also [set up a new OpenXR project without MRTK](new-openxr-project-without-mrtk.md).

## Other non-OpenXR configuration options

**Windows XR**: Microsoft doesn't recommend using the Windows XR plugin for any new projects in Unity 2020. Instead, you should use the Mixed Reality OpenXR plugin. However, if you're using Unity 2019 and you need AR Foundation 2.0 for compatibility with ARCore/ARKit devices, this plugin enables that support.

   > [!IMPORTANT]
   > Using this plugin in Unity 2019 is not compatible with Azure Spatial Anchors.

**Legacy XR**: If you're still on Unity 2019 or earlier, Microsoft recommends using the Legacy Built-in XR support. While the Windows XR plugin is functional on Unity 2019, we don't recommend it  because it's not compatible with Azure Spatial Anchors on Unity 2019.

If you're starting a new project, we recommend that you install Unity 2020 instead and use the Mixed Reality OpenXR plugin.

## Create a new Unity project

1. Launch the **Unity Hub**.
1. In the **Projects** tab,  click **New Project**.

   :::image type="content" source="images/001-new-project.png" alt-text="Screenshot of Unity Hub in Projects tab with the New Project button highlighted.":::

1. Click the drop-down underneath **New project** and then select the Editor version you want.

    :::image type="content" source="images/002-editor-version.png" alt-text="Screenshot of Unity Hub with the Editor version drop-down displayed.":::

1. Ensure the chosen template is **3D Core**.
1. In the **Project name** box, enter a name for your project--for example, "MRTK Tutorial."
1. In the **Location** box, click the folder icon, and then navigate to the folder where you want to save your project and select it. You can also create a new folder.

    :::image type="content" source="images/003-name-and-location.png" alt-text="Screenshot of Unity Hub with 3D, Project Name, Location, and Create highlighted.":::

1. Click **Create Project**. This opens your project in Unity.

    :::image type="content" source="images/004-project-open-in-unity.png" alt-text="Screenshot of your project open in Unity.":::

> [!CAUTION]
> When working on Windows, there is a MAX_PATH limit of 255 characters. Unity is affected by these limits and may fail to compile if any file path is longer than 255 characters. Therefore, we recommend that you store your Unity project as close to the root of the drive as possible.

## Set your build target

1. On the menu bar, select **File** > **Build Settings...**.

    To build an app for Windows Mixed Reality, you must choose a build target. The build settings for Universal Windows Platform (UWP) target any device, including immersive headsets like the [HP Reverb G2](https://www.microsoft.com/en-us/d/hp-reverb-g2-vr-headset/93qb262d0514?activetab=pivot:overviewtab). This is the best choice if you're building for the HoloLens 2; however, if you're targeting desktop VR, we recommend that you use the **PC, Mac & Linux Standalone** platform.

1. Do one of the following:

    **If you're targeting Desktop VR**:
    - Keep the **PC, Mac & Linux Standalone** platform which is selected by default on a new Unity project:

    ![Screenshot of Build Settings window open in the unity editor with PC, Mac & Standalone platform highlighted](images/wmr-config-img-3.png)

    **If you're targeting the HoloLens 2**:
    - Under **Platform**, select **Universal Windows Platform**. Make sure the following settings are active:

    **Target device**: HoloLens

    **Architecture**: ARM64

    **Build Type**: D3D Project

    **Target SDK Version**: Latest Installed

    **Minimum Platform Version**: 10.0.10240.0

    **Visual Studio Version**: Latest installed

    **Build and Run on**: Local Machine

    **Build configuration**: Release (there are known performance issues with Debug)

    ![Screenshot of Build Settings window open in the unity editor with Universal Windows Platform highlighted.](images/030-build-settings-uwp.png)

1. Click the **Switch Platform** button. Unity displays a progress bar while it switches platforms.
1. After the switch platform process is finished, close the **Build Settings** window.

## Download and install the Mixed Reality Feature Tool

 The best way to discover, update, and import feature packages is with the Mixed Reality Feature Tool. You can search packages by name or category, see their dependencies, and view proposed changes to your project's manifest file before importing.

1. Download the latest version of the Mixed Reality Feature Tool from the [Microsoft Download Center](https://aka.ms/MRFeatureTool).
1. After the download finishes, unzip the file and save it to your desktop.

    > [!NOTE]
    > Before you can run the Mixed Reality Feature Tool, you must install the [.NET 5.0 runtime](https://dotnet.microsoft.com/download/dotnet/5.0)

1. In the unzipped folder, navigate to the executable file **MixedRealityFeatureTool.exe** and then use it to launch the Mixed Reality Feature Tool.

    :::image type="content" source="images/open-mixed-reality-feature-tool.png" alt-text="Screenshot of Opening MixedRealityFeatureTool.":::

## Import the Mixed Reality Toolkit and OpenXR packages

1. In the Mixed Reality Feature Tool, select **Start**.

    :::image type="content" source="images/mixed-reality-feature-tool.png" alt-text="Screenshot of the Mixed Reality Feature Tool opening screen.":::

1. Select the Browse button (it's the "three-dot" button in the image below), then navigate to your project, and then open it.

    :::image type="content" source="images/002-open-your-project.png" alt-text="Open your project":::
     
    > [!NOTE]
    > The **Project Path** box in the Tool must contain a value, so it inserts a backslash ("\_") by default.

    After you select a folder, the Tool checks to ensure that it's a valid Unity project folder.

    :::image type="content" source="images/007-project-path.png" alt-text="Screenshot of the Mixed Reality feature Tool Project Path screen.":::
  
1. Select **Discover Features**.

    **Note**: You may need to wait a few seconds while the Tool refreshes the packages from the feeds.

1. On the **Discover Features** page, note that there is a list of six package groups.

    :::image type="content" source="images/003-mrft-groups.png" alt-text="The main groups of packages in the Mixed Reality Feature Tool":::

1. Click the "+" button to the left of **Mixed Reality Toolkit (0 of 10)** and then select the latest version of **Mixed Reality Toolkit Foundation**.

    > [!NOTE]
    > The Mixed Reality Toolkit Foundation package is the only package that must be imported and configured in order to use MRTK with your project. This package includes the core components required to create a mixed reality application.

1. Click the "+" button to the left of **Platform Support (0 of 5)** and then select the latest version of **Mixed Reality OpenXR Plugin**.
 
     :::image type="content" source="images/008-package-selections.png" alt-text="Screenshot of package selections in the Mixed Reality Feature Tool.":::

1. After you've made your selection(s), click **Get Features**.
1. Select **Validate** to validate the packages you selected. You should see a dialog that says **No validation issues were detected**. When you do, click **OK**.
1. On the **Import Features** page, the left-side column, **Features**, displays the packages you just selected. The right-side column, **Required dependencies**, displays any dependencies. You can click the **Details** link for any of these items to learn more about them.
1. When you're ready to move on, select **Import.** On the **Review and Approve** page, you can review information about the packages.
1. Select **Approve.**
1. Return to the Unity Editor and click a blank area in the UI. You'll see a progress bar showing you that your packages are being imported.
 
## Configure OpenXR settings

1. After Unity has imported the packages, a warning appears asking if you want to enable the backends by restarting the editor. Select **Yes**.

    :::image type="content" source="images/unity-restart-option.png" alt-text="Screenshot of Unity Restart Option.":::

1. After Unity reopens, the MRTK Project Configurator should appear. If it doesn't, open it manually: on the menu bar, select **Mixed Reality** > **Toolkit** > **Utilities** > **Configure Project for MRTK**:

    :::image type="content" source="images/009-open-mrtk-configurator.png" alt-text="Screenshot of the menu bar command for opening the MRTK Configurator.":::
    
1. Select **Unity OpenXR Plugin** to enable XR Plugin Management and add the Unity OpenXR Plugin to your project.

    :::image type="content" source="images/010-configurator-select-openxr.png" alt-text="Screenshot of MRTK project configurator window with OpenXR selected.":::

1. The **OpenXR Project Validation** opens. You can ignore this for now.

1. On the **Welcome to MRTK!** screen, select **Show XR Plug-In Management Settings**.

    :::image type="content" source="images/011-show-xr-plugin-management.png" alt-text="Screenshot of the Show XR Plug-In Management Settings button.":::

    This opens the **Project Settings** window.

## Configure the project for desktop VR

If you're developing for the HoloLens2, skip this section and go to the next one, [Configure the project for the HoloLens 2](#configure-the-project-for-the-hololens-2).

1. In the **Project Settings** window, ensure that you're on the **XR Plug-in Management** page and in the **PC, Mac & Linux Standalone** tab.

    :::image type="content" source="images/028-xr-plugin-mgmt-only.png" alt-text="Screenshot of the Project Settings Window open to the XR Plugin Management Page and PC, Mac & Linux Standalone tab.":::

 1. Ensure that **Initialize XR on Startup** is selected, and then, under **Plugin Providers**, click **Open XR**.

    :::image type="content" source="images/031-init-xr-on-startup.png" alt-text="Screenshot of the Project Settings Window, inside the PC, Mac & Linux Standalone tab, with Initialize XR on Startup selected and the OpenXR Plugin highlighted.":::

1. The OpenXR Plugin loads, and then two items appear underneath **OpenXR**. Select the first one, **Windows Mixed Reality feature group**.

    :::image type="content" source="images/032-wmr-feature-group.png" alt-text="Screenshot of Project Settings Window the OpenXR Plugin and Windows Mixed Reality feature group highlighted.":::

Note that there's now a yellow warning triangle next to **OpenXR**. This indicates that you have incompatible settings that need to be resolved. To find out how to address this, skip the next section about configuring the HoloLens 2 and continue on with the following section, [Resolving incompatible settings](#resolving-incompatible-settings).

## Configure the project for the HoloLens 2

1. In the **Project Settings** window, ensure that you're on the **XR Plug-in Management** page with the Universal Windows Platform settings (Windows logo tab) selected.

    :::image type="content" source="images/012-xr-plugin-mgmt-page.png" alt-text="Screenshot of the Project Settings Window open to the XR Plugin Management Page and Universal Windows Platform tab.":::

 1. Ensure that **Initialize XR on Startup** is selected, and then, under **Plugin Providers**, click **Open XR**.

    :::image type="content" source="images/013-init-xr-on-startup.png" alt-text="Screenshot of Project Settings Window 3.":::

1. Two items appear underneath **OpenXR**. Select the first one, **Microsoft HoloLens feature group**.

Note that there's a yellow warning triangle next to **OpenXR**. This indicates that you have incompatible settings that need to be resolved.

## Resolving incompatible settings

The images in this section show the options in the Universal Windows Platform tab. However, the instructions are the same for the Desktop VR tab, except where noted.

1. Hover your cursor over the yellow warning triangle next to **OpenXR**, then read the message in the popup, and then select the triangle.

    :::image type="content" source="images/014-yellow-triangle-warning.png" alt-text="Screenshot of warning about incompatible settings.":::

1. In the **OpenXR Project Validation** window, there are several issues listed. Select the **Fix All** button. **NOTE**: This list may look different depending on which tab you're in.

    :::image type="content" source="images/015-fix-all-button.png" alt-text="Screenshot of the Fix All button in the OpenXR Project Validation window.":::

1. One issue remains and tells you that you must add at least one interaction profile. To do so, click **Edit**. This takes you to the settings for the **OpenXR** plugin in the **Project Settings** window.

    :::image type="content" source="images/016-openxr-screen.png" alt-text="Screenshot of the Project Settings window with the OpenXR settings displayed.":::

1. Underneath **Interaction Profiles**, note the plus sign (+) button.

    :::image type="content" source="images/017-add-profile-button.png" alt-text="Screenshot of the Add Interaction Profile button.":::

 1. Click the button three times, each time choosing a different profile:

    **Eye Gaze Interaction Profile**

    **Microsoft Hand Interaction Profile**

    **Microsoft Motion Controller Profile**

    :::image type="content" source="images/018-interaction-profiles.png" alt-text="Screenshot of interaction profiles that should be added.":::

    If the **Eye Gaze Interaction Profile**, or any other profile, appears with a yellow triangle next to it, select the triangle, and then in the **OpenXR Project Validation** window, click the **Fix** button. When you're finished, close the **OpenXR Project Validation** window.

    :::image type="content" source="images/019-fix-eye-gaze.png" alt-text="Screenshot of the Fix button for the Eye Gaze interaction profile.":::

1. In the **Project Settings** window under **OpenXR Feature Groups**, ensure that the following are selected:
   
   **Microsoft HoloLens**

   **Hand Tracking**

   **Motion Controller Model**

    :::image type="content" source="images/020-selected-features.png" alt-text="Screenshot of selected features for OpenXR.":::

1. Click the **Depth Submission Mode** drop down and then select **Depth 16 Bit**.

    :::image type="content" source="images/021-depth-submission-mode.png" alt-text="Screenshot of Depth 16 Bit selected for Depth Submission Mode.":::

    > [!TIP]
    > Reducing the Depth Format to 16-bit is optional, but it may improve graphics performance in your project. To learn more, see [Depth buffer sharing (HoloLens)](/windows/mixed-reality/mrtk-unity/performance/perf-getting-started#single-pass-instanced-rendering).

    > [!NOTE]
    > The **Render Mode** setting, located just above **Depth Submission Mode**, is set by default to **Single Pass Instanced**. In mixed reality apps, the scene is rendered twice: once for each eye. The result is "stereoscopic vision." This doubles the amount of necessary computing, so it's important to select the most efficient rendering path in Unity to save on both CPU and GPU time. Single pass instanced rendering is the best choice here--we recommend that you enable it by default for every project. To learn more about this, [see the Unity documentation](https://docs.unity3d.com/Manual/SinglePassInstancing.html).

1. Close **MRTK Project Configurator** window.

## Configure Player settings

1. In the **Project Settings** window's left-side column, select **Player**.
1. Note that in the **Player** window, the **Product Name** box is already filled. This is taken from your project name and will be the name displayed in the HoloLens Start menu.

    :::image type="content" source="images/025-product-name.png" alt-text="Screenshot of Unity Publishing Settings with the Project Name box filled in.":::

    > [!TIP]
    > To make the app easier to locate during development, add an underscore in front of the name to sort it to the top of any list.

1. Click the **Publishing Settings** drop down, and then in the **Package name** field, enter a suitable name.

    :::image type="content" source="images/026-package-name.png" alt-text="Screenshot of Unity Publishing Settings with the package name box filled in.":::

    > [!NOTE]
    > The package name is the unique identifier for the app. If you want to avoid overwriting previously installed versions of the app with the same name, you should change this identifier before deploying the app.

1. Close the **Project Settings** window.

### Optimization

If you're developing for HoloLens 2, on the menu bar, select the **Mixed Reality > Project > Apply recommended project settings for HoloLens 2** to get better app performance.

![Screenshot of the mixed reality menu item open with OpenXR selected](images/openxr-img-08.png)

You're now ready to begin developing with OpenXR in Unity!

### Unity sample projects

Check out the [OpenXR Mixed Reality samples repo](https://github.com/microsoft/OpenXR-Unity-MixedReality-Samples) for sample unity projects showcasing how to build Unity applications for HoloLens 2 or Mixed Reality headsets using the Mixed Reality OpenXR plugin.

## See also

- [Set up a new OpenXR project without MRTK](new-openxr-project-without-mrtk.md)
- [Add the Mixed Reality OpenXR Plugin to your existing Unity project](mixed-reality-openxr-plugin.md)
