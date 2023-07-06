---
title: Framework and runtime
description: Information related to framework and runtime in MRTK.
author: keveleigh
ms.author: kurtie
ms.date: 01/12/2021
keywords: Unity,HoloLens, HoloLens 2, Mixed Reality, development, MRTK,
---

# Framework and runtime &#8212; MRTK2

## Changes to the scene

To use the toolkit an instance of the MixedRealityToolkit script must be in your scene.
To add one use the menu option: Mixed Reality Toolkit -> Add to Scene and Configure. This
instance is responsible for registering, updating and tearing down services. It's also
where your configuration profile is chosen.

Apart from adding the MRTK GameObject to the scene the menu option will also:

- Add the MixedRealityPlayspace, which is used by many other MRTK components to reason over
  world and local space transformations.
- Move the main Camera as a child of the MixedRealityPlayspace (and also adding some input and gaze
  related scripts to the main Camera, which help power UnityUI and gaze related input
  functionality).

## MixedRealityToolkit object and runtime

The MRTK has several core services. Some coordinate with one another; others are independent.
All share the same life cycle - startup, registration, update and teardown - and this life
cycle stands apart from Unity's MonoBehaviour life cycle. MRTK has a single
object that manages life and runtime of its services.

This entity ensures that:

- when the game starts, discovery and initialization of services happens in a pre-defined order.
- it provides a mechanism for services to register themselves (i.e. “I support this service!”) and for other
  callers to get a hold of those services.
- it provides the Update()/LateUpdate() calls and forwards them onto the various services
  (i.e. via UpdateAllServices/LateUpdateAllServices).
