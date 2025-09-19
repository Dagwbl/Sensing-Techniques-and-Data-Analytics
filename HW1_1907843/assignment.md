# Sensing Techniques and Data Analytics

## Assignment 1

### Smartphone-Based Sensing of Pendulum Vibrations

**Course:** Sensing Techniques and Data Analytics  
**Instructor:** Mohammad Talebi-Kalaleh  
**Institution:** University of Alberta

-----

### Important Dates

**Submission Deadline:** September 26, 2025, 11:00 AM MST (before class)
*Late submissions may not be accepted*

-----

### 1\. Learning Objectives

Upon completion of this assignment, students will be able to:

  * Utilize smartphone-based sensing capabilities through the PhyPhox application
  * Design and execute controlled pendulum experiments for vibration analysis
  * Apply time-domain analysis techniques to experimental data
  * Compare experimental measurements with theoretical pendulum models
  * Calculate and interpret statistical descriptors of measured signals
  * Identify and analyze sources of measurement error, noise, and nonlinear behavior

**Required Software:** PhyPhox ([https://phyphox.org/download/](https://phyphox.org/download/))

-----

### 2\. Theoretical Background

This assignment requires application of the following theoretical models:

#### 2.1 Small-Angle Pendulum Period

For small angular displacements ($\theta \le 15^\circ$), the period of a simple pendulum is given by:
$$T_{n}=2\pi\sqrt{\frac{L}{g}} \quad (1)$$
where:

  * $T\_n$ = oscillation period (seconds)
  * $L$ = pendulum length (meters)
  * $g$ = gravitational acceleration ($9.81 , m/s^2$)

#### 2.2 Damped Oscillation Model

The amplitude envelope of a damped pendulum follows exponential decay:
$$A(t)=A_{0} \exp(-\zeta\frac{2\pi}{T_{n}}t) \quad (2)$$
where:

  * $A(t)$ = amplitude at time t
  * $A\_0$ = initial amplitude
  * $\zeta$ = damping ratio (dimensionless)
  * $t$ = elapsed time (seconds)

**Figure 1:** Schematic illustration of damped pendulum oscillation.

-----

### 3\. Experimental Setup

#### 3.1 Required Materials

  * Smartphone with PhyPhox installed
  * String (various lengths for L: 0.3m and 1.0m recommended)
  * Toilet paper roll (damping sleeve)
  * Mounting point for pendulum pivot
  * Protractor or angle measurement device
  * Camera for documentation

#### 3.2 Configuration

**Figure 2:** Experimental setup. (a) Schematic diagram showing the pendulum configuration with angle $\theta$, string length L. (b) Example of smartphone inserted into toilet paper roll to prevent rotation. (c) A complete assembled pendulum.

**Setup Instructions:**

1.  Secure string to fixed pivot point
2.  Insert smartphone into toilet paper roll sleeve
3.  Attach phone-sleeve assembly to string end
4.  Ensure pendulum swings in single plane
5.  Configure PhyPhox to record accelerometer data at maximum sampling rate
6.  Focus analysis on axis aligned with swing direction

**Documentation Requirements:** Capture minimum three photographs of your setup from different angles.

-----

### 4\. Required Analysis Tasks

#### 4.1 Part A: Short Pendulum, Small Angles (20%)

1.  **Data Collection:** Perform 10 independent trials
      * Pendulum length: $L \approx 0.3m$
      * Initial angle: $\theta_0 \le 15^\circ$
      * Recording duration: \> 20 oscillations
2.  **Statistical Analysis:** For each trial, compute:
      * Mean ($\mu$)
      * Variance ($\sigma^2$)
      * Root Mean Square (RMS)
      * Skewness ($\gamma_1$)
      * Kurtosis ($\gamma_2$)
3.  **Period Estimation:**
      * Apply autocorrelation or peak-detection algorithms
      * Report mean period and standard deviation across trials: $\overline{T\_n} = T\_n \pm \sigma\_T$
      * Compare with theoretical prediction (Equation 1)
4.  **Damping Analysis:**
      * Extract peak amplitudes over time
      * Using a proper python library, fit exponential decay model (Equation 2) for all 10 trials
      * Report mean damping ratio and standard deviation: $\overline{\zeta} = \zeta \pm \sigma\_\zeta$
5.  **Discussion:** Analyze descriptor robustness and measurement repeatability

#### 4.2 Part B: Long Pendulum, Small Angles (20%)

1.  **Modified Setup:** Increase pendulum length to $L \approx 1.0m$
2.  **Repeat Analysis:** Perform all analyses from Part A
3.  **Comparative Study:**
      * Quantify effect of length on period
      * Compare damping characteristics
      * Assess changes in statistical descriptors

#### 4.3 Part C: Nonlinear Regime Analysis (20%)

1.  **Large-Angle Trials:** Perform 10 trials
      * Return to short pendulum ($L \approx 0.3m$)
      * Initial angle: $\theta_0 > 45^\circ$
2.  **Period Analysis:**
      * Measure period variation with amplitude
      * Quantify deviation from small-angle approximation
      * Plot period vs. amplitude relationship
3.  **Comparison and Discussion:**
      * Compare statistical descriptors with Part A
      * Discuss implications for anomaly detection algorithms

#### 4.4 Part D: Noise Discussion (10%)

1.  **Qualitative Noise Observation:**
      * Visually examine your time-series data for noise patterns
      * Identify any irregular fluctuations or unexpected signal features
      * Comment on the smoothness of the recorded signals
2.  **Discussion:**
      * What are the possible sources of noise in your smartphone measurements?
      * How might noise affect the accuracy of your period and damping estimates?

-----

### 5\. Data Management

#### 5.1 File Structure

```
HW1_{student_id}/
├── HW1_{student_id}.ipynb
├── Data/
│   ├── partA_trial01.csv
│   ├── partA_trial02.csv
│   ├── partB_trial01.csv
│   └── partC_trial01.csv
└── Figures/
    └── (generated plots)
```

#### 5.2 Data Format

  * Export all PhyPhox recordings as CSV files
  * Use descriptive naming convention
  * All analysis code must read directly from `Data/` folder
  * Maintain reproducibility through relative path references

-----

### 6\. Submissions

#### 6.1 Report Requirements

  * **Format:** Jupyter Notebook with integrated analysis (all codes and text in this file)
  * **Length:** Maximum 20 pages (A4) when exported to PDF
  * **Structure:**
  * **Technical Standards:**
      * All equations, figures, and tables numbered with captions
      * Statistical tables rendered as DataFrames (no screenshots)
      * Well-commented, reproducible code
      * Professional presentation quality

#### 6.2 Submission Format

Submit **two files** via course portal:

1.  `HW1_{student_id}.pdf`: Exported notebook
2.  `HW1_{student_id}.zip` containing:
      * Executed `.ipynb` file
      * `Data/` folder with all CSV files
      * `Figures/` folder with all figures

-----

### 7\. Evaluation Criteria

**Table 1:** Grading rubric distribution
| Component | Weight | Key Assessment Points |
| :--- | :--- | :--- |
| Experimental Setup | 10% | Documentation, clarity, reproducibility |
| Part A Analysis | 20% | Accuracy, completeness, interpretation |
| Part B Analysis | 20% | Accuracy, completeness, interpretation |
| Part C Analysis | 20% | Accuracy, completeness, interpretation |
| Part D Discussion | 10% | Accuracy, completeness, interpretation |
| Visualization & Statistics| 10% | Quality, clarity, appropriate methods |
| Professional Presentation | 10% | Organization, formatting, scientific writing |

### Academic Integrity

This assignment must represent your individual work. While discussion of concepts is encouraged, all code, analysis, and written explanations must be your own. Cite any external resources used.