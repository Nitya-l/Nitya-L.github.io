---
layout: default 
title: Synthesized Breath Sounds
permalink: /projects/SynthesizedBreathSounds/
---

# Synthesized Breath Sounds
 
**Bioengineering Senior Capstone** · Department of Bioengineering & CREST Lab, University of Washington <br>
**Team:** Namrata Harish and Natalie Heitkamp <br>
**Mentors:** David Hananel and Dr. Austin Baird <br>
**January 2025 – June 2025**
 
---
 
## Background
 
Auscultation, the act of listening to breath sounds with a stethoscope, is a fundamental clinical skill, but can be difficult to teach. Medical trainees rarely get enough exposure to the full range of pathological breath sounds (wheezing, crackles, stridor, etc.) in controlled educational settings. Medical trainees either practice on real patients or use training manikins with fixed libraries of pre-recorded sounds. However, limited availability of recordings, the lack of diversity, and the inability to customize by patient demographic or disease state makes the teaching process more difficult. This project explored whether generative machine learning models could synthesize clinically realistic breath sounds that are tailored to specific diagnoses and patient demographics to support training manikins and improve clinical education. 

Specifically, we trained a conditional variational autoencoder on open-source lung sound datasets. Model inputs included labels based on patient metadata such as age, sex, disease state, anteroposterior and lateral position of sound acquisition as well as the audio recordings themselves. The core pipeline converted the raw audio signal into mel spectrograms and paired each spectrogram with the encoded metadata. The trained model could then take a user-defined patient profile as input and output a generated mel spectrogram, which was then reconstructed into audio using the Griffin-Lim algorithm. 

## My Contributions
**Data acquisition, preprocessing, and management**: I was jointly responsible (with Namrata) for sourcing, cleaning, and preparing the datasets. This included writing the code for extracting and collating patient metadata from separate metadata files and audio filenames, converting audio samples to mel spectrograms, and building the data pipeline that tied each sample to its encoded patient profile using Python's Pickle module.
 
**Model architecture and iteration**: I took the lead on implementing and iterating on the CVAE model architecture. The base model came from starter code built for musical instrument sound generation and I extended it to handle multi-feature conditioning across the full patient profile. Over the course of the project, Namrata and I moved through six model iterations that considered various aspects of the input data based on literature searches on wavefrom versus spectrogram based audio-generation and signal-processing technqiues. 
 
**User testing implementation**: Contributed to implementing the quantitative user study — a 10-question Google Forms quiz where participants matched generated spectrograms to original patient profiles. Results showed 35.4% average accuracy (vs. 30% chance), confirming the model had not yet learned to generate condition-distinguishable sounds.
 
---
 
## Poster
 
![Synthesized Breath Sounds Capstone Poster](/assets/images/CapstonePoster.pdf)
 
*Presented at the University of Washington Department of Bioengineering Senior Capstone Showcase, June 2025.*
 
---

## My Takeaways 
This was the most technically open-ended project I have ever worked on and it strengthened my ability to work through the iterative nature of machine learning model development. Most of my coursework in machine learning had focused on traditional classification and predictive modeling tasks, along with the underlying statistical and computational principles, rather than generative models.

While the decision to utilize a generative modeling approach for this project was our own, it required us to independently explore unfamiliar literature, evaluate competing methodologies, and adapt existing techniques to a novel biomedical application. As a result, I gained experience not only in implementing machine learning models, but also in navigating the uncertainty that comes with open-ended research questions where there is no clear roadmap to follow. Although our final model was unable to generate clinically distinguishable breath sounds, the project reinforced the value of iterative experimentation and taught me how to critically assess model performance, identify limitations, and use unsuccessful results to guide future improvements. As I continue pursuing biomedical research, I hope to apply the technical skills developed through this project alongside my wet-lab experience to build more comprehensive approaches to developing new therapeutic strategies.
