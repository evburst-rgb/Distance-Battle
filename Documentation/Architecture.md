# Distance Battle
## Software Architecture
### Created by EvBurst

---

# Overview

Distance Battle is built as a modular BakkesMod plugin.

Every major game feature is isolated into its own system to improve readability, testing, and future expansion.

The GameManager acts as the central controller for all gameplay.

---

# System Overview

Distance Battle

├── Core
├── DistanceTracker
├── StartGate
├── CameraController
├── HUD
├── ProgressBoard
├── SaveManager
├── ResetManager
├── AudioManager
└── Utilities

---

# Core

Responsible for:

• Plugin initialization

• Game loop

• System startup

• System shutdown

• Communication between systems

Primary Classes

DistanceBattle

Plugin

GameManager

---

# DistanceTracker

Responsible for:

• Flight path calculation

• Live distance

• Official rounded distance

• Ground detection

Input

Ball Position

Output

Flight Distance

Official Distance

---

# StartGate

Responsible for:

• Detecting when the ball crosses the gate

• Starting flight tracking

• Triggering gate animation

• Triggering gate audio

---

# CameraController

Responsible for:

• Follow ball

• Hold camera after landing

• Return camera

• Camera transitions

---

# HUD

Responsible for:

• Live distance

• Official distance

• Progress display

• Result popup

---

# ProgressBoard

Responsible for:

• Remaining numbers

• Completed numbers

• Shrinking board

• Progress counter

---

# SaveManager

Responsible for:

• Saving progress

• Loading progress

• Resetting progress

---

# ResetManager

Responsible for:

• Ball reset

• Player reset

• Camera reset

• Round restart

---

# AudioManager

Responsible for:

• Start Gate audio

• Success audio

• Dead Zone audio

• UI sounds

---

# Utilities

Shared helper functions.

Examples

Distance math

Logging

Configuration

File helpers

Debug tools

---

# Game Flow

Player Hits Ball

↓

Ball Crosses Start Gate

↓

Distance Tracking Begins

↓

Camera Follows Ball

↓

Ball Lands

↓

Distance Calculated

↓

HUD Updated

↓

Progress Saved

↓

Camera Returns

↓

Ball Reset

↓

Next Attempt

---

# Development Philosophy

Every system has one responsibility.

Every feature is modular.

Every milestone is tested before moving forward.

No feature is added unless it improves the player experience.

Every Meter Matters.