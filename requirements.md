# System Requirements

## Functional Requirements
1. **Primary ID Scanning:** The system shall authenticate a voter by scanning a primary identification token (e.g., MyKad/Voter ID barcode or QR code) at the polling kiosk.
2. **Guided Capture UI:** The system shall capture live facial frames using a guided capture interface that provides real-time on-screen framing, alignment, and distance feedback to the voter.
3. **Image Quality Assessment (IQA) Gate:** The system shall execute a pre-authentication FIQA filter to verify sharpness, resolution, and ambient illumination before invoking downstream liveness verification.
4. **Multimodal Liveness Detection:** The system shall perform passive facial liveness detection by analyzing physical texture features and micro-expressions to prevent presentation attacks (photos/screens).
5. **Structured Audit Logging:** The system shall generate structured, anonymized audit logs and standard error codes for every authentication transaction to assist election administrators with turnout reconciliation.

## Non-Functional Requirements
1. **Performance & Throughput:** The entire kiosk authentication workflow (from ID scan to ballot authorization) shall complete within 15 seconds per voter to prevent queue bottlenecks during peak hours.
2. **Reliability & Usability:** The system shall maintain an acceptable False Rejection Rate (FRR) under varied indoor lighting environments by utilizing automated IQA pre-filtering and structured retry mechanisms.
3. **Security & Privacy:** The system shall ensure data isolation and anonymize audit trails, guaranteeing that no direct link exists between biometric authentication logs and cast ballots.
