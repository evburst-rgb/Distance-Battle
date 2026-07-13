# Distance Battle
## Coding Standards
### Created by EvBurst

---

# Purpose

This document defines the coding standards for the Distance Battle project.

Every contributor should follow these standards to keep the codebase clean, readable, and maintainable.

---

# Philosophy

- Keep code simple.
- One class, one responsibility.
- One function, one purpose.
- Readability is more important than cleverness.
- Every Meter Matters.

---

# File Organization

Each system should live in its own folder.

Example

Plugin/
    CameraController/
    DistanceTracker/
    HUD/
    ProgressBoard/
    SaveManager/

Do not place unrelated code inside another system.

---

# Class Naming

Classes use PascalCase.

Examples

DistanceTracker

GameManager

CameraController

StartGate

HUD

ProgressBoard

---

# Function Naming

Functions use PascalCase.

Examples

StartTracking()

StopTracking()

UpdateDistance()

ResetRound()

LoadProgress()

SaveProgress()

UpdateHUD()

---

# Variable Naming

Variables use camelCase.

Examples

currentDistance

officialDistance

ballInFlight

cameraTransitionTime

remainingObjectives

---

# Constant Naming

Constants use ALL_CAPS.

Examples

MAX_DISTANCE

MIN_DISTANCE

DEADZONE_MIN

DEADZONE_MAX

MAX_FLIGHT_DISTANCE

---

# Boolean Naming

Boolean variables should read naturally.

Examples

isTracking

isCameraFollowing

hasBallLanded

isRoundComplete

Avoid vague names.

Bad

tracking

camera

Good

isTracking

isCameraFollowing

---

# Comments

Explain WHY.

Do not explain WHAT.

Bad

// Increase distance by 1

Good

// Flight distance is accumulated every game tick while the ball is airborne.

---

# Magic Numbers

Avoid hard-coded values.

Instead use named constants.

Bad

if(distance > 250)

Good

if(distance >= FINAL_DISTANCE)

---

# Formatting

Use consistent indentation.

Keep braces on their own lines.

Example

if (isTracking)
{
    UpdateDistance();
}

---

# Responsibilities

Every class should have one responsibility.

DistanceTracker

Calculates flight distance.

Nothing else.

CameraController

Moves the camera.

Nothing else.

HUD

Displays information.

Nothing else.

---

# Git Commits

Every completed feature receives its own commit.

Examples

Added Start Gate detection

Implemented Distance Tracker

Added Camera Controller

Updated HUD animations

Avoid commits such as:

"Stuff"

"Changes"

"Fix"

---

# Testing

Every feature must be tested before merging into main.

If it cannot be tested, it is not complete.

---

# Development Philosophy

Every Meter Matters.

Every Milestone Matters.

Build systems.

Not shortcuts.