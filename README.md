# Human-Computer Interaction (HCI) — Projects & Prototypes

[![Figma Prototype](https://img.shields.io/badge/Figma-Interactive%20Prototype-F24E1E.svg?logo=figma&logoColor=white)](https://www.figma.com/proto/VmwdEbkfVBAM2bRtJR2kEj/L04G02?node-id=0-1&t=15Ww1N0VZqUnA8yM-1)
[![Language](https://img.shields.io/badge/Language-JavaScript%20(ES6)-yellow.svg)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Library](https://img.shields.io/badge/Library-p5.js-ed225d.svg)](https://p5js.org/)
[![Database](https://img.shields.io/badge/Database-Firebase-orange.svg)](https://firebase.google.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A collection of interactive prototypes and experimental user interfaces developed as part of the **Human-Computer Interaction (Interfaces Pessoa-Máquina — IPM)** course at **Instituto Superior Técnico (IST), Universidade de Lisboa**.

This repository showcases two core challenges:
1. **Bake-Off #1:** UI/UX Design & High-Fidelity Mobile App Prototype in Figma.
2. **Bake-Off #2:** High-speed dense target selection engine built in JavaScript with p5.js under Fitts's Law constraints.

---

## Bake-Off 1: Recipe Social Network (Mobile UI/UX Prototype)

<p align="center">
  <a href="https://www.figma.com/proto/VmwdEbkfVBAM2bRtJR2kEj/L04G02?node-id=0-1&t=15Ww1N0VZqUnA8yM-1">
    <img src="https://img.shields.io/badge/Test_Interactive_Prototype-Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white" alt="Test on Figma" height="40" />
  </a>
</p>

### The Problem
Traditional video-sharing platforms (like TikTok or YouTube) lack specialized interfaces for culinary content. Users struggle to filter recipes based on seasonal availability, dietary restrictions, or the specific kitchen utensils they actually own.

### The Solution: High-Fidelity Interactive Prototype
An interactive mobile app concept reimagining recipe discovery and cooking guidance:
* **Kitchen Utensil Profiling:** Users configure their home equipment profile, and the app automatically filters out recipes requiring unavailable utensils.
* **Seasonal & Local Discovery:** Smart search highlighting recipes featuring in-season fruits, vegetables, and ingredients.
* **Dietary & Allergen Customization:** Preset profiles for vegan, vegetarian, gluten-free, and allergen-free culinary exploration.
* **Cooking Mode & Video Feed:** Distraction-free interactive video player paired with step-by-step cooking timelines.

### UX Research & Usability Evaluation
* **Formative User Testing:** Conducted iterative user evaluations using **Think-Aloud Protocols** and **Wizard of Oz** methodologies to identify cognitive bottlenecks and optimize navigation flows.
* **Quantitative Evaluation:** Validated user satisfaction and usability using the **User Experience Questionnaire (UEQ-S)**, scoring high benchmark ratings in perspicuity and efficiency.

**[Launch Interactive Mobile Prototype in Figma](https://www.figma.com/proto/VmwdEbkfVBAM2bRtJR2kEj/L04G02?node-id=0-1&t=15Ww1N0VZqUnA8yM-1)**

---

## Bake-Off 2: Dense UI Target Selection (p5.js Implementation)

An interactive, experimental canvas application designed for high-speed, high-accuracy target acquisition across densely populated interactive displays (80 targets in an 8x10 grid).

### Theoretical Background: Fitts's Law
In human-computer interaction, targeting performance is bounded by **Fitts's Law**:

$$T = a + b \log_2 \left( \frac{2D}{W} \right)$$

Where movement time $T$ increases as target width $W$ decreases and distance $D$ increases. In dense layouts, visual clutter and small target dimensions drastically increase error rates.

### Design Strategies & Techniques
* **Visual Categorization:** High-contrast color mapping and grouped spatial layouts to accelerate pre-attentive visual search.
* **Auditory Feedback (`synth`):** Immediate audio cues triggered on target confirmation, eliminating latency in visual verification.
* **Live Telemetry & Evaluation:** Quantitative measurement of trial execution time, successful hits, misses, selection accuracy (%), average acquisition time per target, and penalty scoring.
* **Optional Firebase Sync:** Realtime Database logging is disabled by default (`RECORD_TO_FIREBASE = false`) with placeholder configuration in `index.html`. Connect your own Firebase Realtime Database instance by updating `firebaseConfig`.

### Project Structure (Bake-off #2)
```text
hci-prototypes-and-benchmarks/
├── index.html              # Canvas host page and p5.js dependencies
├── sketch.js               # Main interaction loop, grid layout, trial logic
├── target.js               # Target entity representation and hit testing
├── support.js              # Evaluation metrics and experiment control routines
├── ppi.js                  # Display calibration and physical dimension scaling
├── style.css               # Canvas layout and typography
├── legendas/               # Target label CSV dataset files
├── LICENSE                 # MIT License
└── README.md               # Project documentation
```

### Running Bake-Off #2 Locally
No build process or installation is required:
* **Option 1:** Open `index.html` directly in any modern browser.
* **Option 2:** Launch a local development server:
  ```bash
  python3 -m http.server 8000
  ```
  Navigate to `http://localhost:8000`.

---

## Authors & Acknowledgments

* **David Vasques** ([@DeastV](https://github.com/DeastV))
* **Guilherme Marques** ([@marques-jpg](https://github.com/marques-jpg))

Collaborative group project developed for Interfaces Pessoa-Máquina (IPM) at Instituto Superior Técnico, Universidade de Lisboa.

*Course-Provided Resources:* Display calibration utilities (`ppi.js`, `support.js`, `target.js`) and target label sets (`legendas/`) were provided by the IPM teaching faculty. The MIT License applies to the student implementation, custom interaction design, auditory synthesis, and Figma prototypes.

