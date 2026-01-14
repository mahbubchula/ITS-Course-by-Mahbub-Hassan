# Module 6: Traffic Control Systems

!!! abstract "Learning Objectives"
    By the end of this module, you will be able to:
    
    1.  Compare different signal control algorithms (Pre-timed vs. Actuated vs. Adaptive).
    2.  Understand the detection technologies that drive traffic control.
    3.  Implement strategies for system optimization and emergency operations.

---

## 1. Signal Control Algorithms

How does a traffic light "decide" when to change?

### A. Pre-timed Control
*   **Method:** Fixed cycle lengths (e.g., 60s Green, 30s Red) based on historical data.
*   **Best for:** Intersections with very predictable traffic (e.g., downtown grids).
*   **Cons:** Very inefficient when traffic is light; people wait at red lights for no reason.

### B. Actuated Control
*   **Method:** Uses sensors (detectors) to "see" cars. If a car is waiting, it gives a green light.
*   **Best for:** Intersections where side-street traffic is irregular.
*   **Pros:** Reduces unnecessary delay.

### C. Adaptive Control (The "Smart" Way)
*   **Method:** Uses AI and real-time data to adjust timings every few seconds across a whole network.
*   **Systems:** SCATS, SCOOT, InSync.
*   **Pros:** Reduces congestion by up to 25% by coordinating multiple lights.

---

## 2. Detection Technologies

If the signal is the "mouth," the detector is the "eye."

=== "Inductive Loops"
    *   **How:** Wire coils buried in the pavement. They sense the metal in a car.
    *   **Pros:** Extremely accurate, works in all weather.
    *   **Cons:** Road must be cut to install; breaks if the road cracks.

=== "Video Detection (VDS)"
    *   **How:** Cameras with software that draws "virtual loops" on the screen.
    *   **Pros:** Easy to install; can also count bikes and pedestrians.
    *   **Cons:** Struggling in heavy rain, fog, or shadows.

=== "Radar/LiDAR"
    *   **How:** Emits waves to detect objects.
    *   **Pros:** Excellent in all weather; can track speed very accurately.
    *   **Cons:** More expensive.

---

## 3. System Optimization

The goal of optimization is to minimize **Delay** and **Stops**.

!!! info "Green Waves (Coordination)"
    By timing lights so that a "platoon" of cars hits every green light at a specific speed (the "Progression Speed"), we create a green wave. This significantly reduces fuel consumption and emissions.

```mermaid
graph LR
    A[Light 1: Green] --- B[Light 2: Green] --- C[Light 3: Green]
    Note over A,C: Cars move at 50km/h without stopping
```

---

## 4. Emergency Operations

In an emergency, the normal rules of traffic must change instantly.

*   **Emergency Vehicle Preemption (EVP):** An ambulance or fire truck sends a signal (Optical, GPS, or Radio) to the light, forcing it to turn Green immediately.
*   **Railroad Preemption:** When a train is coming, all traffic signals near the tracks must clear the tracks of cars immediately.
*   **Fail-Safe Mode:** If the signal controller detects an error, it defaults to **Flash Red** in all directions to prevent accidents.

---

## ✅ Module 6 Checkpoint

??? check "Test your knowledge"
    **Q1: Which signal control method is best for a city experiencing highly unpredictable traffic surges?**
    
    - [ ] Pre-timed
    - [ ] Actuated
    - [x] Adaptive
    
    **Q2: What happens if a traffic signal controller detects a major internal error?**
    
    - [ ] It turns all lights Green.
    - [ ] It turns all lights off.
    - [x] It enters "Fail-Safe" mode (Flash Red).
