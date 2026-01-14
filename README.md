# Project Plan & Team Split  
## Assistive Smart Glasses for Blind / Deafblind Navigation

### Project Overview
This project develops lightweight smart glasses that assist blind (and optionally deafblind) users with real-time environmental awareness. The system detects obstacles, movement, and hazards, then communicates guidance through **audio (bone conduction)** and **haptics**. Heavy computation is offloaded wirelessly to reduce weight on the glasses.

---

## Core Problem Being Solved
Blind and deafblind individuals lack **continuous, real-time spatial awareness** when navigating unfamiliar or dynamic environments. Current tools (white canes, guide dogs, static audio apps) are:
- Reactive, not predictive  
- Limited in spatial resolution  
- Ineffective for deafblind users  

This project solves **active, anticipatory navigation assistance** using computer vision + multimodal feedback.

---

## System Architecture (High Level)
- **On-glasses:** ESP32-S3 + camera(s) + haptic motors  
- **Offloaded compute:** Smartphone or Raspberry Pi (wireless)  
- **Feedback:**  
  - Audio (bone-conduction earbuds)  
  - Haptics (directional vibration cues)

---

## Team Role Split

### 1. Heth – Hardware, CAD, System Integration (Lead)
**Responsibilities:**
- Select and validate hardware components:
  - ESP32-S3-CAM modules
  - Camera modules (mono or stereo decision)
  - Haptic motors & drivers
  - Bone-conduction audio interface
- Design **CAD model of the glasses**:
  - Camera placement (bridge / temples)
  - Cable routing
  - Weight distribution
  - Comfort & wearability
- Define power system:
  - Battery selection
  - Charging method
  - Runtime estimation
- Ensure all hardware communicates reliably with ESP32
- Final system integration & testing

**Deliverables:**
- Hardware BOM with costs
- Wiring diagrams
- CAD files (.STEP / .STL)
- Physical prototype fit assessment

---

### 2. Ashwin – Software, Vision & Intelligence
**Responsibilities:**
- Computer vision pipeline:
  - Obstacle detection
  - Motion detection (approaching objects)
  - Left/right localization
- Threat classification logic:
  - Moving vs static hazards
  - Distance thresholds
- Convert vision output → instructions:
  - Example: “Bicycle approaching from left”
- Optimize for real-time performance
- Decide between:
  - On-device ML (lightweight)
  - Offloaded processing (phone / Pi)

**Deliverables:**
- Vision algorithm documentation
- Demo outputs (images / logs)
- Latency benchmarks
- Threat detection accuracy analysis

---

### 3. Adrian – UX, Accessibility & Feedback Systems
**Responsibilities:**
- Design feedback logic for:
  - Blind users (audio + haptics)
  - Deafblind users (haptics only)
- Haptic language design:
  - Directional vibrations
  - Intensity vs distance
  - Emergency patterns
- UI/UX flow for phone-based setup:
  - Voice-first interaction
  - Zero-vision operation
- User safety & ethical considerations

**Deliverables:**
- UX flow diagrams
- Haptic pattern reference chart
- Accessibility justification
- User testing scenarios

---

## Timeline & Milestones (8 Weeks)

### Week 1 – Research & Lock Decisions
- Finalize problem scope
- Lock system architecture
- Decide phone vs Raspberry Pi compute
- Confirm camera strategy (mono vs stereo)

**Deliverable:** System Design Doc

---

### Week 2 – Hardware & CAD Start
- Order components
- Initial CAD sketches
- Power budget estimation

**Deliverable:** BOM + CAD draft v1

---

### Week 3 – Vision Prototype
- Basic object detection running
- Test camera feeds
- Latency measurement

**Deliverable:** Vision demo video/logs

---

### Week 4 – Wireless Integration
- ESP32 → phone/Pi communication
- Data packet structure defined
- Real-time streaming test

**Deliverable:** Communication protocol doc

---

### Week 5 – Feedback Systems
- Haptics integrated
- Audio cues implemented
- Directional alerts tested

**Deliverable:** Feedback demo

---

### Week 6 – Full System Assembly
- Final CAD print
- Hardware mounted
- End-to-end system working

**Deliverable:** Working prototype

---

### Week 7 – Testing & Iteration
- Indoor & outdoor testing
- Edge cases (crowds, bikes, stairs)
- UX refinement

**Deliverable:** Test results + improvements

---

### Week 8 – Presentation & Submission
- Poster
- Technical report
- Demo script
- Judges’ Q&A prep

**Deliverable:** Final submission package

---

## Competitive Strength (CWSF Relevance)
- Real-world impact
- Strong engineering depth
- Accessibility-focused design
- Clear innovation beyond existing tools
- Scalable and defensible

---

## Notes
- System intentionally modular
- Works for blind **and** deafblind users
- Phone-based compute keeps glasses light
- No reliance on cloud = privacy-safe

---
