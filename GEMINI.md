# GEMINI.md - HeadPaint

## Project Overview
**HeadPaint** is an iOS application that allows users to create digital paintings using the movement of their head while listening to music via AirPods. The core concept is mapping head motion data (pitch, yaw, roll) to brush strokes on a canvas, creating a unique visual artifact for every song session.

* **Platform:** iOS (SwiftUI)
* **Core Hardware:** AirPods (Motion Tracking via `CMHeadphoneMotionManager`)
* **Pricing:** Free (No IAP/Payment logic required)

---

## 🧠 Master Rules & Workflow

### 1. Development Methodology: TDD (Strict)
* **Red-Green-Refactor:** You must strictly follow Test-Driven Development.
* **Step 1:** Write a failing unit test or UI test for the specific feature or logic.
* **Step 2:** Run the test to confirm failure.
* **Step 3:** Implement the minimum code necessary to pass the test.
* **Step 4:** Refactor for cleanliness and security.

### 2. Git & Version Control
* **Branching:** strictly create a new branch for every ticket.
    * Format: `feature/ticket-{number}-{short-description}`
* **Pull Requests:** Do not merge code directly.
    * When a ticket is finished, generate a Pull Request (PR) summary for me to review.

### 3. Task Management
* **Ticket Naming:** Sequential integers (e.g., `Ticket-1`, `Ticket-2`).
* **Tracking:** The **Master Ticket List** below must be updated immediately upon picking up a task or finishing one.
* **Structure:** Each ticket must include a **Description** and specific **Implementation Steps**.

### 4. Security & Best Practices
* Ensure all permissions (Motion, Audio) are handled with proper `Info.plist` usage descriptions and runtime checks.
* Data privacy: Ensure motion data is processed locally and not exported without user intent.
* Follow Apple's Human Interface Guidelines (HIG).

---

## 📋 Master Ticket List

### 🛑 Backlog (To Do)
* [ ] **Ticket-2:** Headphone Motion Manager Service (TDD)
* [ ] **Ticket-3:** Basic Canvas View Implementation
* [ ] **Ticket-4:** Audio Player & Permission Handling
* [ ] **Ticket-5:** Mapping Motion Data to Brush Strokes

### 🚧 In Progress
* **Ticket-1:** Project Initialization & CI Setup

### ✅ Completed
* *None*

---

## 📂 Active Ticket Details

### **Ticket-1:** Project Initialization & CI Setup
See [Ticket-1.md](file:///Users/keno/Desktop/test/HeadPaint/tickets/Ticket-1.md) for details.

---

## 📚 Completed Tickets Archive

*Move completed ticket details here for history tracking.*

---

## 🛠 Feature Specifications (Reference)

### Core Motion Logic
* **Manager:** `CMHeadphoneMotionManager`
* **Data Points:**
    * *Pitch* (Vertical head tilt) -> Controls Y-axis / Brush Thickness?
    * *Yaw* (Horizontal head turn) -> Controls X-axis / Color Hue?
    * *Roll* (Head tilt sideways) -> Controls Opacity / Stroke Style?
* *Note:* Need a calibration step to center the user's head before painting starts.

