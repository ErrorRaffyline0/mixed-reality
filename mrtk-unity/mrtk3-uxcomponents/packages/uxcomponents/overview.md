---
title: UX Components
description: Overview of the UX Components package
author: Zee2
ms.author: finnsinclair
ms.date: 6/6/2022
ms.localizationpriority: high
keywords: Unity,HoloLens, HoloLens 2, Mixed Reality, development, Button, PressableButton, Slider, Toggle
---

# UX Components &#8212; MRTK3

This package contains an extensive library of pre-built UX prefabs ready for use in your mixed reality applications.

If you'd like to only consume the underlying UX scripts (for example, if you're building your own custom UX component libraries) you should only take a dependency on the [UX Core](../../../mrtk3-uxcore/packages/uxcore/overview.md) package. UX Core doesn't include any dependencies on our assets, visuals, or solvers. If you're building your own custom UX components, you can avoid unnecessary dependencies in your project by only consuming UX Core.

The UX Components package includes ready-to-use prefabs for [Canvas](../../../mrtk3-uxcore/packages/uxcore/canvas-ui.md) layout environments. These prefabs implement the new [Mixed Reality Design Language](mixed-reality-design-language.md).

These prefabs use all of the [RectTransform](https://docs.unity3d.com/ScriptReference/RectTransform.html) layout, alignment, and design tools that Unity offers as part of [Unity UI](https://docs.unity3d.com/Manual/com.unity.ugui.html). We strongly recommend that developers [gain familiarity with the UI tooling that already exists as part of Unity](https://learn.unity.com/tutorial/working-with-ui-in-unity), as experience with Unity UI will also apply to building UI with MRTK3.

While Canvas-based UI will be the right choice for most situations, it might not always be the best fit for your application. Certain workloads can see improved performance by using non-Canvas-based UI rendering, such as some UI layouts where massively batched rendering can reduce drawcalls. [For more information, see this comparison table.](../../../mrtk3-uxcomponents-noncanvas/packages/uxcomponents-noncanvas/overview.md)