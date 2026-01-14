# Module 4: ITS Data Management

!!! abstract "Learning Objectives"
    By the end of this module, you will be able to:
    
    1.  Design database architectures suitable for high-volume traffic data.
    2.  Implement analytics platforms to derive insights from raw data.
    3.  Establish robust information security and backup protocols.

---

## 1. Database Architecture for ITS

ITS generates **massive** amounts of data—from video feeds to millisecond sensor readings. A standard Excel sheet won't cut it. We need specialized architectures.

### Types of Databases Used
*   **Relational Databases (SQL):** Good for structured data like user accounts or toll transactions.
    *   *Example:* PostgreSQL, Oracle.
*   **Time-Series Databases (TSDB):** Essential for sensor data where time is the key index.
    *   *Example:* InfluxDB. *Why?* Because querying "Show me traffic speed every minute for the last year" is instant.
*   **NoSQL / Data Lakes:** For unstructured data like raw video logs or social media text.

---

## 2. Analytics Platforms & Processing

Data is useless unless we process it.

### The Processing Pipeline
1.  **Ingestion:** Getting data from the road to the server (e.g., via Kafka).
2.  **Cleaning:** Removing errors (e.g., a sensor reporting 500 km/h).
3.  **Analytics:**
    *   **Descriptive:** "What happened?" (Traffic jam at 5 PM).
    *   **Predictive:** "What will happen?" (Based on history, traffic will jam tomorrow).
    *   **Prescriptive:** "What should we do?" (Change signal timing to prevent the jam).

---

## 3. Storage Solutions & Backup

### Storage Tiers
*   **Hot Storage (SSD):** Data needed *right now* (e.g., current signal status). Fast but expensive.
*   **Warm Storage (HDD):** Data from last week. Slower access.
*   **Cold Storage (Tape/Glacier):** Archival data from 5 years ago. Very cheap, very slow.

### System Backup Strategies
*   **Full Backup:** Copying everything every night. (High storage use).
*   **Incremental Backup:** Copying only what changed since the last backup. (Efficient).
*   **RAID (Redundant Array of Independent Disks):** Storing data across multiple hard drives so if one fails, no data is lost.

---

## 4. Information Security in Data

Protecting the integrity and privacy of data is paramount.

!!! warning "Privacy Concerns"
    We collect license plates (ALPR) and travel patterns. This is sensitive **PII (Personally Identifiable Information)**.
    
    *   **Anonymization:** Removing names/IDs from data before analysis.
    *   **Encryption at Rest:** Encrypting the hard drive itself.
    *   **Encryption in Transit:** Using HTTPS/TLS when sending data over the network.

---

## ✅ Module 4 Checkpoint

??? check "Test your knowledge"
    **Q1: Which type of database is best for storing sensor readings collected every second?**
    
    - [ ] Relational SQL
    - [x] Time-Series Database
    - [ ] Excel Spreadsheet
    
    **Q2: What is "Cold Storage" used for?**
    
    - [ ] Data needed immediately for real-time control.
    - [x] Archiving old data that is rarely accessed.
    - [ ] Cooling down the server room.
