# Dense UI Target Selection — HCI Bake-Off

[![Language](https://img.shields.io/badge/Language-JavaScript%20(ES6)-yellow.svg)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Library](https://img.shields.io/badge/Library-p5.js-ed225d.svg)](https://p5js.org/)
[![Field](https://img.shields.io/badge/Field-Human--Computer%20Interaction%20(HCI)-blue.svg)]()
[![Backend](https://img.shields.io/badge/Database-Firebase-orange.svg)](https://firebase.google.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

An experimental user interface developed for high-speed, high-accuracy target acquisition in densely populated interactive displays (80 targets in an 8x10 grid). 

Developed as part of the **Bake-Off #2 Challenge** in the **Human-Computer Interaction (Interfaces Pessoa-Máquina)** course at **Instituto Superior Técnico (IST), Universidade de Lisboa**.

---

## The Challenge

In human-computer interaction, selecting targets in dense graphical interfaces is bounded by **Fitts's Law**:

$$T = a + b \log_2 \left( \frac{2D}{W} \right)$$

Where acquisition time $T$ increases as target width $W$ decreases and distance $D$ increases. 

In this challenge, users must find and click 12 sequential target items out of an 80-item grid (8 rows by 10 columns) as quickly and accurately as possible under real-time timing constraints.

---

## Design Strategies & Interaction Techniques

* **Visual Guidance & Color Coding:** Intelligent categorization and high-contrast color highlights to guide the user's focal visual search across the dense matrix.
* **Auditory Feedback (`synth`):** Audio cue generation upon target selection to minimize visual confirmation delay and reduce user error rate.
* **Effective Target Area Optimization:** Expanded bounding boxes and predictive hover affordances to minimize cursor movement penalties.
* **Empirical Data Logging:** Integration with **Google Firebase** to record real-time trial durations, hit counts, miss counts, and calculate overall user throughput.

---

## Project Structure

```
.
├── index.html              # Canvas host page and p5.js dependencies
├── sketch.js               # Main interaction loop, grid layout, trial logic
├── target.js               # Target entity representation and hit testing
├── support.js              # Evaluation metrics and experiment control routines
├── ppi.js                  # Display calibration and physical dimension scaling
├── style.css               # Clean full-screen canvas styling
├── legendas/               # Target label CSV dataset files
├── LICENSE                 # MIT License
└── README.md               # Project documentation
```

---

## How to Run

No build step or complex tooling is needed. You can run the application directly in your browser:

### Option 1: Direct File
Simply open `index.html` in any modern web browser (Chrome, Firefox, Safari, Brave).

### Option 2: Local HTTP Server (Recommended)
```bash
# Using Python
python3 -m http.server 8000
```
Open `http://localhost:8000` in your browser.

---

## Authors

* **David Vasques** ([@DeastV](https://github.com/DeastV))
* **Guilherme Marques** ([@marques-jpg](https://github.com/marques-jpg))

*Instituto Superior Técnico — Universidade de Lisboa (2025/2026)*
