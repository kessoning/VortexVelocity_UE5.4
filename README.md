# Niagara Vortex Velocity Module (UE 5.4+)

This repository contains a custom Niagara Module Script asset for Unreal Engine 5.4 and later (tested on 5.4 and 5.5). It recreates the functionality of the **Vortex Velocity** module, which was removed from the engine starting with version 5.4.

## Problem

The standard Vortex Velocity module, useful for creating swirling particle motion, is no longer included in Unreal Engine 5.4+. This can break existing projects migrating from older versions or prevent users from easily achieving this common effect in new projects.

## Solution

This custom Niagara Module Script (`.uasset`) provides a direct replacement for the missing module.

* **Functionality:** Replicates the behavior and parameters of the original Vortex Velocity module.
* **Compatibility:** Designed for **Unreal Engine 5.4** and **Unreal Engine 5.5**. It should work in future versions unless Niagara's scripting backend changes significantly.

## Motivation

I frequently used the Vortex Velocity module in my own projects. Upon migrating to UE 5.4, I discovered it was missing. Seeing online discussions from other developers looking for solutions or ways to recreate it, I decided to package the recreated version I made for my own use and share it here.

## How It Was Made

The process to recreate this was straightforward:
1.  Opened Unreal Engine 5.3.
2.  Created a new Niagara Emitter and added the standard `Vortex Velocity` module.
3.  Double-clicked the `Vortex Velocity` module to open its underlying script graph.
4.  Copied the entire graph/logic.
5.  Created a new **Niagara Module Script** asset in an Unreal Engine 5.4 project.
6.  Pasted the copied graph/logic into the new Module Script.
7.  Cleaned up inputs/outputs and tested to ensure it functions correctly.

## Installation & Usage

1.  **Download:** Get the `.uasset` file from this repository.
2.  **Import:** Drag and drop the downloaded `.uasset` file directly into the Content Browser of your Unreal Engine 5.4+ project.
3.  **Add to Niagara System:**
    * Open your Niagara Emitter or System.
    * Navigate to the stack group where you want to add the velocity (e.g., Particle Update).
    * Click the `+` button to add a module.
    * Search for the name of this custom module.
    * Alternatively, you can drag the imported Module Script asset directly from the Content Browser onto the Niagara stack.
4.  **Configure:** Adjust the parameters exposed in the module (like Vortex Axis, Amount, etc.) just like you would with the original module.
