# Final Project – VIGIL: Autonomous ICU Patient Monitoring Agent

## Overview
This project presents **VIGIL (Vital Intelligence Guardian for ICU Lifesaving)**, a conceptual autonomous AI agent designed to monitor ICU patients in real time and detect early signs of deterioration.

The system focuses on improving patient outcomes by identifying critical changes in vital signs before they become life-threatening, while reducing alarm fatigue for healthcare staff.

## Problem
In ICU environments, clinicians must monitor multiple patients at once, tracking vital signs such as:
- Heart rate
- Blood pressure
- Oxygen saturation (SpO₂)
- Respiratory rate
- Temperature

However:
- Up to 70% of ICU alarms are false positives
- Early warning signs of deterioration are often subtle
- High workload leads to delayed response times

This creates a gap between **patient deterioration and clinical intervention**, which VIGIL is designed to solve :contentReference[oaicite:0]{index=0}.

## Solution – VIGIL System
VIGIL is an **AI-driven autonomous monitoring agent** that:
- Continuously analyzes patient vital signs
- Detects abnormal patterns in real time
- Generates explainable alerts for clinicians
- Supports decision-making without replacing human control

## System Architecture
The system uses a **four-tier architecture**:

1. **Sensors (Tier 1)**
   - ECG, SpO₂, blood pressure monitors, temperature probes
   - Collect real-time patient data

2. **Edge Node (Tier 2)**
   - Performs real-time anomaly detection
   - Runs lightweight AI models for fast response

3. **Hospital Server (Tier 3)**
   - Processes alerts and integrates with EHR systems
   - Runs more complex AI models

4. **Cloud Layer (Optional Tier 4)**
   - Used for model retraining and analytics

📊 The architecture diagram (page 4) shows how data flows from sensors → edge → server → clinician dashboards :contentReference[oaicite:1]{index=1}.

## AI Components
The system combines three AI models:

- **TimeGAN (Generative Model)**
  - Generates synthetic data for rare events like sepsis or cardiac arrest

- **LSTM Autoencoder (Edge Model)**
  - Detects anomalies in real-time using patient-specific patterns

- **Clinical Language Model (LLM)**
  - Converts alerts into clear, human-readable explanations

## Alert System
VIGIL uses a **3-level escalation framework**:

- **WATCH** → minor anomaly (no interruption)
- **ESCALATE** → moderate risk (notify nurse)
- **EMERGENCY** → critical condition (immediate alert)

The system provides recommendations but **does not take autonomous medical action**, ensuring human oversight.

## Security & Ethics
This system prioritizes:
- **HIPAA compliance**
- **Data privacy (on-premise processing)**
- **End-to-end encryption (TLS 1.3, AES-256)**
- **Bias monitoring across patient groups**
- **Explainable AI outputs**

## Testing & Performance Goals
The system was designed with the following targets:

- >92% alert sensitivity
- >85% specificity
- <90 seconds alert latency
- <100ms edge inference time
- 99.9% system uptime

📈 The testing scenarios (page 12) include stress testing, security validation, and anomaly detection simulations :contentReference[oaicite:2]{index=2}.

## Challenges & Trade-Offs
- Limited real-world data for rare events
- Hardware constraints on edge devices
- Complexity of EHR integration
- Need for clinical validation and regulatory approval

## Key Takeaways
- AI can significantly improve early detection in healthcare
- Edge computing is critical for real-time decision-making
- Explainability is essential for trust in medical AI
- Human oversight must always remain in control

## Simple Reflection
This project helped me understand how complex real-world AI systems are, especially in healthcare. It’s not just about building a model—it’s about designing a full system that is reliable, secure, and usable by people. I also learned how important explainability and ethics are when AI is used in critical environments like the ICU.
