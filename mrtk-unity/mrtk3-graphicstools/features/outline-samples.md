---
title: MeshOutline Sample Scene
description: Illustrated walkthrough of the MeshOutline examples
author: Species521
ms.author: wettigmarti
ms.date: 06/23/2022
ms.localizationpriority: medium
keywords: Unity, HoloLens, HoloLens 2, Mixed Reality, development, MRTK, Graphics Tools, MRGT, MR Graphics Tools, Standard Shader, Animation, MeshOutlines, Outlines
---

# MeshOutline Examples

This scene illustrates the outline feature and its variation possibilities.
Outlines are a quick and appealing feature you can use to highlight objects in a scene.
In addition to color and thickness, we can define the highlighting by adding animations and gradient effects.

![Screenshot of several objects with outlines.](images/SampleScenes/OutlinesScene_01.gif)

To achieve the outline effect, add the MeshOutline script for single objects or the MeshOutlineHierarchy script for entire mesh hierarchies. Adjust the Outline Width to your needs and apply an outline material.

![Screenshot of options in the MeshOutline and MeshOutlineHierarchy scripts.](images/SampleScenes/outlineScripts_side-side_01.png)

For guides on how to set up an outline material, see [MeshOutline Material Setup](https://github.com/Species521/mixed-reality-pr_mawettig/blob/main/mrtk-unity/mrtk3-graphicstools/features/mesh-outlines.md#material-setup[)

## Outline Pulse Example

![Screenshot of a rectangular object with a pulsating outline.](images/SampleScenes/OutlinesRainbow_01.gif)

In this example, the Outline Width value is animated and applied to the object itself as Animator 'OutlinePulseController'.

![Screenshot of the Animator with the Controller option set to OutlinePulseController](images/SampleScenes/pulseAnimation_01.jpg)

> [NOTE]
> Depending on the model's edge hardness, you might experience jagged and disrupted results. For the Outline effect to work properly, the model's vertex normals need to be smooth. If the model itself doesn't provide this, try an in-editor solution: apply the MeshSmoother script to the model.
> [Learn more about the MeshSmoother](mesh-outlines.md#mesh-smoothing).

![Screenshot of the MeshSmoother component with the Smooth Normals on Awakening option turned on.](images/SampleScenes/MeshSmoother_01.jpg)

## Hierarchies and multiple and skinned meshes

![Screenshot of an animated cat with an outline.](images/SampleScenes/OutlinesCat_01.gif)

Some imported 3D objects come in multiple parts in hierarchical structures. In this case, the model has several sub-nodes, such as skeletal joints and unattached additional meshes. In order to avoid searching and applying through the entire hierarchy, you can add the MeshOutlineHierarchy script to the root object and then all meshes inside that structure will have the effect applied as well.
As seen in this example, the outline works very well on skinned and animated meshes, too.

## Illumination effects

![Screenshot of a doughnut-shaped object, also called a torus, outlined with an orbiting Proximity Light.](images/SampleScenes/OutlinesReveal_01.gif)

In this example, the outlines are illuminated by an orbiting Proximity Light, which is part of both the MRTK and the MRGT. Highlight size, color, gradients and intensity are configurable. 
To learn more about the Proximity Light, see the [Proximity Light Overview](proximity-light.md) and [Proximity Lighting Example](https://github.com/Species521/mixed-reality-pr_mawettig/blob/graphics-tools-docs/mrtk-unity/mrtk3-graphicstools/features/samples/material-gallery.md#hover-lights)

## See also

* [Standard Shader](https://github.com/MicrosoftDocs/mixed-reality-pr/blob/main/mrtk-unity/mrtk3-graphicstools/features/standard-shader.md)
* [Material Gallery](https://github.com/MicrosoftDocs/mixed-reality-pr/blob/main/mrtk-unity/mrtk3-graphicstools/features/samples/material-gallery.md)
