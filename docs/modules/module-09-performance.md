# Module 9: System Performance Analysis

!!! abstract "Learning Objectives"
    By the end of this module, you will be able to:
    
    1.  Select appropriate measurement methods and performance metrics.
    2.  Apply analysis techniques to identify system bottlenecks.
    3.  Develop reporting systems and improvement plans based on data.

---

## 1. Measurement Methods

We cannot manage what we do not measure. Performance analysis tells us if our investment in ITS is actually working.

### Data Sources
*   **Direct:** Sensors, GPS probes, and Bluetooth readers.
*   **Indirect:** Fuel consumption data, accident records, and air quality sensors.

---

## 2. Key Performance Metrics (KPIs)

| Metric | Definition | Why it matters |
| :--- | :--- | :--- |
| **Travel Time** | Time to go from A to B. | Primary concern for drivers. |
| **Delay** | Travel Time - Free Flow Time. | Measures the cost of congestion. |
| **Reliability** | How much travel time varies day to day. | Crucial for logistics and buses. |
| **Queue Length** | How many cars are waiting at a light. | Indicates signal inefficiency. |
| **Safety** | Number of "Near-Miss" events or crashes. | The ultimate goal of ITS. |

---

## 3. Analysis Techniques

### Bottleneck Analysis
Using a **Heatmap** to see where speeds drop consistently. If speeds drop at the same spot every day, it's a **Recurring Bottleneck** (Design issue). If it happens randomly, it's **Non-Recurring** (Incident/Weather).

### Before-and-After Studies
Comparing data from *before* an ITS upgrade (e.g., installing Adaptive Control) to *after*.
*   *Example:* "After installing the green wave, average travel time dropped by 12%."

---

## 4. Reporting & Visualization

Data must be understandable to decision-makers (mayors, engineers, public).

*   **Dashboards:** Real-time speed maps (like Google Maps) for operators.
*   **Annual Reports:** High-level summaries for the public.
*   **Bencmarking:** Comparing your city's performance to other cities.

---

## 5. Improvement Planning

Once an issue is identified (e.g., high delay at Intersection X), we plan an improvement:
1.  **Optimization:** Adjust signal timing (Low cost).
2.  **Technology:** Add better sensors (Medium cost).
3.  **Infrastructure:** Add a new lane (High cost).

---

## ✅ Module 9 Checkpoint

??? check "Test your knowledge"
    **Q1: What is the difference between Travel Time and Delay?**
    
    - [ ] They are the same.
    - [x] Delay is the extra time spent over the ideal "Free Flow" time.
    - [ ] Delay is only measured at traffic lights.
    
    **Q2: If a bottleneck happens at the same time every Monday morning, what is it called?**
    
    - [x] Recurring Bottleneck
    - [ ] Non-recurring Bottleneck
    - [ ] Random event
