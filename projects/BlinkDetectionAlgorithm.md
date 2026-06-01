---
layout: default
title: Blink Detection Algorithm
permalink: /projects/BlinkDetectionAlgorithm/
---
# Blink Detection Algorithm
 
**Graduate Research Assistant** · Center for Language and Speech Processing, Johns Hopkins University
**September 2025 – June 2026**
---
 
## Background
 
One of the projects at the Center for Language and Speech Processing focuses on using machine learning algorithms to identify neurodegenerative diseases such as Alzheimer’s or Parkinson’s based on a series of writing, speech, and eye-movement–based tasks that patients are asked to perform. Within the realm of eye-movement, saccades, which are rapid eye movements between fixation points, are indicative of underlying neurological function and can reflect abnormalities in motor control and cognitive processing consistent with neurodegenerative conditions. One challenge in this work is accurately differentiating regular blink patterns from saccades. As such, my work at the CLSP focused on developing and refining an automated blink detection algorithm intended to support the clinical tool for the early diagnosis of neurodegenerative diseases. 

---
 
## My Contributions
 
**Algorithm development**: Developed and validated a blink detection algorithm that processes eye-tracking video data to accurately identify and characterize blink events usig pupil size as the primary signal. The method uses a rolling median baseline and adaptive thresholding to identify rapid pupil-size drops consistent with blink evets. Signals from both eyes are processed independently and then merged ad refined using statistical consistentcy checks to improve robustness. The output is structured as a set of blink onset and offset timestamps. This process involved feature engineering, threshold tuning, and validation against ground-truth labeled data.
 
**Device transition support**: Contributed to the migration of existing data processing pipelines between different eye-tracking hardware platforms, ensuring consistency in data format, resolution, and temporal alignment across devices.
 
---

## My Takeaways
 
While this project is far removed from the rest of my wet-lab based work, it helped strengthen my coding and data analysis skills, particularly in working with real-world, noisy data. It also gave me the opportunity to explore areas beyond wet-lab workflows in a computational research setting. Working through this pipeline improved my ability to debug and refine algorithmic logic based on empirical performance rather than theoretical expectations. 
