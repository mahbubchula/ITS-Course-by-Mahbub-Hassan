# Module 7: Network Security Architecture

!!! abstract "Learning Objectives"
    By the end of this module, you will be able to:
    
    1.  Conduct a basic threat assessment for ITS infrastructure.
    2.  Implement security protocols including access control and encryption.
    3.  Develop incident response and recovery procedures for cyber-attacks.

---

## 1. Threat Assessment

ITS is considered **Critical Infrastructure**. A cyber-attack on a traffic signal system could cause physical harm.

### Common Threats
*   **Spoofing:** Sending fake data to a traffic controller (e.g., making it think a car is there when it isn't).
*   **Denial of Service (DoS):** Overwhelming the network so the TMC cannot control the lights.
*   **Ransomware:** Locking the TMC servers and demanding money to restore traffic operations.
*   **Physical Tampering:** Opening a roadside cabinet and plugging in a rogue device.

---

## 2. Security Protocols & Access Control

How do we stop the "bad actors"?

### The "Zero Trust" Model
Assume everything is a threat until proven otherwise.

1.  **Access Control:** Only authorized employees can log into the TMC. Use **Multi-Factor Authentication (MFA)**.
2.  **Network Segmentation:** Keep the traffic light network separate from the office Wi-Fi. If a virus hits an office laptop, it shouldn't reach the signals.
3.  **Firewalls & VPNs:** All field devices should connect to the TMC via an encrypted **VPN (Virtual Private Network)**.

---

## 3. Encryption Methods

Encryption is the process of scrambling data so only the intended receiver can read it.

*   **AES (Advanced Encryption Standard):** Used for "Data at Rest" (on hard drives).
*   **TLS/SSL:** Used for "Data in Transit" (moving across the fiber/wireless network).
*   **Public Key Infrastructure (PKI):** Used in V2X to ensure that messages from vehicles are authentic (as seen in Module 3).

---

## 4. Incident Response & Recovery

When an attack happens, every second counts.

!!! danger "The Response Plan"
    1.  **Identification:** Use an **IDS (Intrusion Detection System)** to spot unusual traffic patterns.
    2.  **Containment:** Isolate the infected part of the network immediately.
    3.  **Eradication:** Remove the malware or rogue device.
    4.  **Recovery:** Restore systems from the **clean backups** we made in Module 4.
    5.  **Audit:** Analyze how they got in and patch the hole.

---

## 5. Audit Processes

Regularly testing your own security is the best defense.
*   **Penetration Testing:** Hiring "White Hat" hackers to try and break into the system.
*   **Vulnerability Scanning:** Using software to find outdated devices that need security updates (patches).

---

## ✅ Module 7 Checkpoint

??? check "Test your knowledge"
    **Q1: What is "Network Segmentation"?**
    
    - [ ] Cutting the fiber optic cable.
    - [x] Separating the critical control network from general office networks.
    - [ ] Adding more nodes to a network.
    
    **Q2: Why is Multi-Factor Authentication (MFA) important for TMC operators?**
    
    - [ ] It makes logging in faster.
    - [x] It ensures that even if a password is stolen, the hacker cannot get in without a second code.
    - [ ] It saves electricity.
