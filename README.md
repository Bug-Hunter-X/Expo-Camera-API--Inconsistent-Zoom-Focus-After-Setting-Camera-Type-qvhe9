# Expo Camera API: Inconsistent Zoom/Focus After Setting Camera Type

This repository demonstrates a bug encountered when using the Expo Camera API.  The issue involves inconsistent access to zoom and focus features after setting the camera type (front or back).  The behavior is unpredictable, sometimes working correctly and sometimes failing without clear indication.

## Bug Description

The bug is reproducible when using the Expo `Camera` API, specifically when accessing zoom and focus functionality after initially setting the `cameraType` prop.  In some instances, zoom and focus will function as expected.  Other times, calls to `zoomInAsync`, `zoomOutAsync`, `setFocusDepthAsync`, or similar will either fail silently or throw an error.

## Reproduction

The `bug.js` file contains a minimal reproducible example that showcases this behavior.  Run the example and observe the erratic response to zoom and focus actions.

## Solution

The `bugSolution.js` provides a potential workaround. This example may involve modifying state handling or carefully managing the order of operations when interacting with the Camera API.