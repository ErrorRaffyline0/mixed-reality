---
title: Mixed reality feature samples and apps
description: Stay up to date with all the available Microsoft sample apps and mixed reality features samples for HoloLens.
author: qianw211
ms.author: vinnietieto
ms.date: 03/10/2022
ms.topic: article

keywords: mixed reality, unity, tutorial, hololens, learn, samples, MRTK, research mode, HoloLens 2, qr codes, mixed reality capture, holographic remoting, UX Tools
ms.localizationpriority: high
---

# Mixed reality feature samples and apps

![Picture of a user wearing a HoloLens and manipulating a hologram with hand movement](unreal/images/unreal-developer.jpg)

Every development journey starts with a look back at what other developers have successfully built - mixed reality is no different. Currently, all of our tutorials and sample apps are built in Unity or Unreal. As we develop content for other engines and platforms, you'll find them under the relevant heading in the Table of Contents.

* [Sample application case studies](#sample-application-case-studies)
* [Feature samples](#feature-samples)

## Sample application case studies

[!INCLUDE[](includes/tabs-samples.md)]

## Feature samples

For each of the developer scenarios listed below, there are feature samples that correspond to specific implementations that are covered in our documentation and cover a range of development platforms and hardware devices.

| Scenario | Feature sample | Engine | Description |
| --- | --- | ---- | --- |
| [**Build basic Unity mixed reality scenarios**](#build-basic-openxr-scenarios) | [OpenXR with Unity samples](#build-basic-openxr-scenarios) | Unity C# | Get started with cross-platform developer tools using the latest Unity 2020.LTS and OpenXR plugin. |
| [**Anchoring Strategies**](../design/spatial-anchors.md) | [Local anchor](https://github.com/microsoft/OpenXR-Unity-MixedReality-Samples#sample-for-anchors-and-anchor-persistence) |  | Persist and share spatial anchors across application sessions and across devices. See the [Spatial anchors](../design/spatial-anchors.md) article. |
|    | [Azure Spatial Anchors samples](https://github.com/Azure/azure-spatial-anchors-samples) |  | Build spatially aware mixed reality applications with the essential capabilities of [Azure Spatial Anchors](/azure/spatial-anchors/overview). |
| | [QR Codes](#qr-codes) | Unity C# | Detect QR Codes in the environment. |
| [**Collaboration in mixed reality**](#collaboration-in-mixed-reality) | [User identity](#user-identity) | Unity C# | Set up your HoloLens 2 device using Azure Active Directory (AAD) credentials. |
| | [Azure Spatial Anchors samples](https://github.com/Azure/azure-spatial-anchors-samples) |  | Build spatially aware mixed reality applications with the essential capabilities of [Azure Spatial Anchors](/azure/spatial-anchors/overview). |
| [**Spatial interaction**](#spatial-interaction---basic-hologram-sample) | [Basic hologram sample](#spatial-interaction---basic-hologram-sample) | Windows 10 C++ | Render a spinning cube in Windows Mixed Reality. |
|  [**Scene/Object understanding**](#scene-understanding) | [Scene understanding samples](#scene-understanding) | Unity C# | Help design environmentally-aware mixed reality applications. |
|    | [Azure Object Anchors samples](https://github.com/Azure/azure-object-anchors) | Unity C# | Detect an object in the physical world using a 3D model and estimate its 6DoF pose with [Azure Object Anchors](/azure/object-anchors/overview). |
| [**Contextual data overlays**](#contextual-data-overlays) | [QR Codes](#qr-codes) | Unity C# | Detect QR Codes in the environment. |
| | [Poster tracker sample](#poster-tracker-sample)  | Unity C# | Align a hologram with a real world object. |
| | [Build mixed reality digital twins](#build-mixed-reality-digital-twins) | Unity C# | Learn how to create a mixed reality application using Azure Digital Twins and Unity, a real-time 3D platform. |
| [**Capturing camera data**](#camera-captures) | [Mixed reality capture sample](#holographic-mixed-reality-capture) | Windows 10 C++ | Capture the first-person experience of mixing real and digital worlds as a photo or video. |
| | [Research Mode samples](#research-mode) | Windows 10 C++ | Access to key sensors on a HoloLens device for research applications. |
| [**Holographic Remoting**](#holographic-remoting) | [Holographic Remoting player](#holographic-remoting) |  Windows 10 C++ | Stream holographic content from a PC to your Microsoft HoloLens in real time by using a Wi-Fi connection. |
| | [Azure Remote Rendering samples](/azure/remote-rendering/samples/sample-model) | Unity C# | Test the Azure Remote Rendering service by using the resources for sample data listed here. |
| **Task management and guidance** | [Dynamics 365 Remote Assist](/dynamics365/mixed-reality/remote-assist/ra-overview) | | Collaborate more efficiently by working together from different locations with Dynamics 365 Remote Assist on HoloLens, HoloLens 2, Android, or iOS devices. |
| | [Dynamics 365 Guides](/dynamics365/mixed-reality/guides/) | | Help operators learn during the flow of work by providing holographic instructions when and where they're needed. |
| **World Locking holograms** | [World locked physics sample](/mixed-reality/world-locking-tools/documentation/howtos/samples/worldlockedphysicssample) | Unity C# | Explore a few virtual physics experiences that are enabled by World Locking Tools' world-locked coordinate system. |
| | [Space pin sample](/mixed-reality/world-locking-tools/documentation/howtos/samples/spacepin) | Unity C# | Move closer to the inner workings of a real-world application that needs to align a large object or objects with real-world features. The Space Pin sample offers a simplified and more focused view of the Space Pin feature.  |
| | [Ray pins example](/mixed-reality/world-locking-tools/documentation/howtos/samples/raypins) | Unity C# | Demonstrate how to set up Space Pins by manually manipulating marker objects into position using MRTK affordances. |
| | [World Locking Tools with Azure Spatial Anchors sample](/mixed-reality/world-locking-tools/documentation/howtos/samples/wlt_asa_sample) | Unity C# | Provide a stable coordinate system that can be persisted across sessions and shared across devices in your application.  This is made possible when combining World Locking Tools for Unity (WLT) with Azure Spatial Anchors (ASA). |
| Managing Power and Thermals |  [Managing Power & Thermals](unity/managing-power-and-thermals.md) | Unity C#, Win32 C++ | When the HoloLens 2 is running in warm environments or with heavy performance requirements (CPU/GPU usage, peripheral usage, etc.), PowerThermalNotification SDK can be used to subscribe to notification events, allowing the device to operate longer. See the [PowerThermalNotification API reference](/dotnet/api/microsoft.mixedreality.powerthermalnotification). |

### Build basic OpenXR scenarios

If you're new to building basic mixed reality scenarios, these samples will help you to getting started.

For developers targeting Unity 2020 to build HoloLens 2 or mixed reality applications, the OpenXR Plugin can be used instead of the Windows XR Plugin for better cross-platform compatibilities. The Mixed Reality OpenXR Plugin also works well with the latest version of the Mixed Reality Toolkit (2.7.x).

| Sample | Reference article | Platform | Description | 
| --- | --- | --- | --- |
| [Mixed Reality OpenXR with Unity samples](https://github.com/microsoft/OpenXR-Unity-MixedReality-Samples) | [Using the OpenXR plugin](unity/new-openxr-project-with-mrtk.md) |  Unity C# | These sample projects showcase how to build Unity applications for HoloLens 2 or Mixed Reality headsets using the Mixed Reality OpenXR plugin. <br> <br> The following sample scenarios are covered: <br> <ul> <li> [Using hand tracking joints and mesh inputs in Unity](https://github.com/microsoft/OpenXR-Unity-MixedReality-Samples#sample-for-hand-tracking) </li> <li> [Using anchor and anchor persistence](https://github.com/microsoft/OpenXR-Unity-MixedReality-Samples#sample-for-anchors-and-anchor-persistence) </li> <li> [Using ARPlaneManager on HoloLens2](https://github.com/microsoft/OpenXR-Unity-MixedReality-Samples#sample-for-arfoundation-compatibility) </li> <li> [Using ARRaycastManager on HoloLens2](https://github.com/microsoft/OpenXR-Unity-MixedReality-Samples#sample-for-arfoundation-compatibility) </li> <li> [Using eye tracking on HoloLens2](https://github.com/microsoft/OpenXR-Unity-MixedReality-Samples#sample-for-eye-tracking) </li> <li> [Using locatable camera in unity](https://github.com/microsoft/OpenXR-Unity-MixedReality-Samples#sample-for-locatable-camera)  </li> |
| [OpenXR MRTK Base Unity project](https://github.com/microsoft/UnityOpenXRMRTKBase) | See [sample readme](https://github.com/jessemcculloch/UnityOpenXRMRTKBase#unityopenxrmrtkbase) |  Unity C# | This repo contains a Unity project that is set up with the Microsoft Mixed Reality Toolkit Foundations and Standard Assets packages and the Microsoft OpenXR Plugin package. |
| [Using Unity 2020.3 and MRTK 2.7.2](https://github.com/microsoft/MixedRealityToolkit-Unity#example-scenes) | [What is MRTK](/windows/mixed-reality/mrtk-unity/) | Unity C# | MRTK-Unity is a Microsoft-driven project that provides a set of components and features that are used to accelerate cross-platform MR app development in Unity. |
| [OpenXR Explorer](https://github.com/maluoi/openxr-explorer#msdynttrid=udu2MjGd1z293SGMmgAul0BalrUKvy4iwBnBrc3lEn4) | See [sample readme](https://github.com/maluoi/openxr-explorer#openxr-explorer) | C++, Windows, Linux, OpenXR | OpenXR Explorer is a handy debug tool for OpenXR developers. It allows for easy switching between OpenXR runtimes, shows lists of the runtime's supported extensions, and allows for inspection of common properties and enumerations, with direct links to relevant parts of the OpenXR specification! |
| [OpenXR Samples for Mixed Reality Developers](https://github.com/microsoft/OpenXR-MixedReality) | [What is OpenXR](../develop/native/openxr.md#what-is-openxr) |  C++ | These OpenXR samples use C++17 and Direct3D 11. The same source code works across UWP applications running on HoloLens 2 and Win32 applications running on Windows Desktop with Windows Mixed Reality immersive headsets. |

### Collaboration in mixed reality

In mixed reality, people come together virtually to share experiences and collaborate.  Samples listed here demonstrate some features that make such collaboration possible.

#### User identity 

This sample sets up your HoloLens 2 device using Azure Active Directory (AAD) credentials, and then configures the device to use iris login.

| Sample | Reference article | 
| --- | --- |
| [AAD Login on HoloLens 2](https://github.com/peted70/aad-hololens) | [Overview of Microsoft identity platform](/azure/active-directory/develop/v2-overview) | 

### Spatial interaction - basic hologram sample

This sample runs on Windows Mixed Reality and renders a spinning cube. You can interact with the cube by placing it in a new position, and various input methods are allowed. This sample works on PCs with headset devices attached, and also on Microsoft HoloLens.

|  Sample | Reference article |
| --- | --- |
| [Windows Universal samples - basic hologram](https://github.com/microsoft/Windows-universal-samples/tree/main/Samples/BasicHologram) | See [sample readme](https://github.com/microsoft/Windows-universal-samples/tree/main/Samples/BasicHologram#basic-hologram-sample) | 

### Scene understanding

Scene understanding provides Mixed Reality developers with a structured, high-level environment representation.  Scene understanding is designed for developing intuitive and environmentally aware applications, by combining the power of existing mixed reality runtimes. These runtimes are the highly accurate but less structured spatial mapping and new AI driven runtimes.

| Sample | Reference article |  Platform | Description |
| --- | --- | --- | --- |
| [Mixed Reality Scene Understanding samples (SU SDK)](https://github.com/microsoft/MixedReality-SceneUnderstanding-Samples) | [Scene understanding](../design/scene-understanding.md) | Unity C# and SU SDK | A Unity-based sample application that showcases Scene Understanding on HoloLens 2. |
| [Scene Understanding sample (MRTK + SU SDK)](https://github.com/microsoft/MixedRealityToolkit-Unity/blob/main/Assets/MRTK/Examples/Experimental/SceneUnderstanding/Scenes/SceneUnderstandingExample.unity) | [Scene understanding observer (MRTK)](/windows/mixed-reality/mrtk-unity/features/spatial-awareness/scene-understanding) | Unity C#, MRTK + SU SDK | MRTK + Scene Understanding SDK sample. |

### Contextual data overlays

Contextual data is the background information that provides a broader understanding of an event, person, or item.  With Augmented Reality (AR), this information can be displayed and precisely aligned with physical objects to provide insights, instructions, service records, and other important data.

#### QR codes

HoloLens 2 can detect QR codes in the environment around the headset, establishing a coordinate system at each code's real-world location.

| Sample | Reference article | 
| --- | --- |
| [QR code tracking in Unity](https://github.com/microsoft/MixedReality-QRCode-Sample) | [QR codes](advanced-concepts/qr-code-tracking-overview.md) | 

#### Poster tracker sample

It is often helpful to be able to align a hologram to a real-world object, or align multiple HoloLens devices to a common set of world coordinates, so that everyone sees the same holograms in the same location. For instance, in your Unity scene, you can add a "poster" where you want to anchor your scene (perhaps a game board), and then add holograms on or around it. Then you can print the poster, lay it on a table, and run the calibration/alignment tool, which will move the holographic version of the poster so that it aligns with the physical version of the poster. This moves all of the linked holograms to the correct alignment.

| Sample | Reference article | 
| --- | --- |
| [Poster calibration sample](https://github.com/microsoft/MixedRealityCompanionKit/tree/master/PosterCalibrationSample) | See [sample readme](https://github.com/microsoft/MixedRealityCompanionKit/tree/master/PosterCalibrationSample#postercalibrationsample) | 

#### Build mixed reality digital twins

In this sample, you'll learn how to create a mixed reality HoloLens 2 application using Azure Digital Twins and Unity, a real-time 3D platform. 

| Sample | Reference article | 
| --- | --- |
| [Building mixed reality digital twins with Azure Digital Twins and Unity](https://github.com/MicrosoftDocs/mslearn-mr-adt-in-unity) | [Full learning path](/training/paths/build-mixed-reality-azure-digital-twins-unity/) | 


### Camera captures

Unstructured environment sensor data that your Mixed Reality device captures are converted into powerful abstract or holographic representations of the physical world around us. 

#### Holographic Mixed Reality Capture

Mixed reality capture (MRC) captures the first-person experience of the combined real and digital worlds as a photo or video and shares what you see with others in real time.

| Sample | Reference article | 
| --- | --- |
| [Mixed Reality Capture samples](/samples/microsoft/windows-universal-samples/holographicmixedrealitycapture/) | [Mixed Reality Capture](advanced-concepts/mixed-reality-capture-overview.md) | 

#### Research Mode

Research Mode was introduced in the first-generation HoloLens to give access to key sensors on the device, specifically for research applications that are not intended for deployment. The sample applications below are examples for accessing and recording Research Mode streams and using the [intrinsic and extrinsic](/windows/mixed-reality/locatable-camera#locating-the-device-camera-in-the-world).

| Sample application | Reference article | 
| --- | --- |
| [HoloLens (first gen)](https://github.com/microsoft/HoloLensForCV/tree/master/Samples) | [Research Mode](advanced-concepts/research-mode.md) | 
| [HoloLens 2](https://github.com/microsoft/HoloLens2ForCV/tree/main/Samples) | [Research Mode](advanced-concepts/research-mode.md) | 

### Holographic Remoting

The Holographic Remoting Player is a companion app that connects to PC apps and games that support Holographic Remoting. Holographic Remoting streams holographic content from a PC to your Microsoft HoloLens in real time using a Wi-Fi connection, and is supported on HoloLens (first gen) and HoloLens 2.


| Sample | Reference article | 
| --- | --- |
| [Holographic Remoting samples](https://github.com/microsoft/MixedReality-HolographicRemoting-Samples) | [Holographic Remoting Overview](./native/holographic-remoting-overview.md) |
