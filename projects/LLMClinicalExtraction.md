---
format: default
title: LLM Clinical Extraction
permalink: /projects/LLMClinicalExtraction/
---
# LLM-Assisted Annotation and Biomarker Feature Extraction for NSCLC Immunotherapy Resistance
 
**Team Lead & First Author** · Precision Care Medicine Course Project, Johns Hopkins University <br>
**Collaborators:** Sean Li, Eric Guan, Weiyao Tao, Marcus Torres-Negron, Isha Yeleswarapu <br>
**Faculty Advisors:** Dr. Joseph Greenstein, Dr. Casey Overby Taylor, Dr. Siamak Ardekani <br>
**Clinical Collaborator:** Dr. Joseph Murray (Sidney Kimmel Comprehensive Cancer Center / Caris Life Sciences) <br>
**September 2025 – June 2026**
 
---

 
## Background
 
Approximately 64% of non-small cell lung cancer (NSCLC) patients who respond to immune checkpoint inhibitors eventually develop resistance but mechanisms are still poorly understood. Predicting who will respond, and for how long, requires integrating multiple types of clinical data: radiology reports, blood test results, treatment histories, and outcomes. The problem is that most of this data lives in unstructured text or heterogeneous longitudinal records that cannot easily be fed into a machine learning pipeline. Radiographic reports and laboratory biomarkers each carry signals about treatment response, but they are more valuable together than apart. Standard methods for extracting structured information from radiology reports are slow, annotation-intensive, and don't scale. At the same time, longitudinal CBC and metabolic panel data contain patterns tied to immunotherapy outcomes that aren't visible from any single timepoint. The goal of this project was to develop a structured extraction and feature identification pipeline that could feed into future multimodal predictive models for immunotherapy resistance.
 
This project took a two-pronged approach to that problem. As team lead and first author, I coordinated the overall project and led the LLM extraction component myself. Biomarker clustering and predictive modeling from lab records was carried out by teammates under the same collaborative framework.

---
 
## My Contributions: LLM Extraction Pipeline
 
**Project leadership**: Led a multidisciplinary team of five students and coordinated project direction with faculty advisors and clinical collaborators. Oversaw project planning, research execution, and manuscript preparation.
 
**LLM evaluation and prompt engineering**: Designed and executed a systematic evaluation of multiple large language models for structured extraction of clinical variables from radiology reports. Developed prompting strategies and implemented the code used to automate model querying through the secure institutional AI platform (HOPGPT).
 
**Semantic similarity scoring**: Implemented a semantic similarity scoring pipeline using ClinicalBERT-based BERTScore to compare model-generated annotations against oncologist-generated ground truth. Evaluated alternative scoring approaches and selected the final evaluation methodology used in the study. 
 
**Output preprocessing and normalization**: Helped developed preprocessing workflows to standardize model outputs and convert free-text clinical information into structured variables suitable for downstream analysis.
 
**Statistical analysis**: Wrote the code for and performed the statistical analysis used to evaluate extraction performance. Applied linear mixed-effects models and multiple-comparison correction methods to assess the effects of model selection, prompting strategy, and inference parameters on annotation accuracy.
 
---

## Team Contributions (Biomarker Component)
 
A few of my teammates conducted a parallel analysis on longitudinal complete blood count (CBC) and comprehensive metabolic panel (CMP) records from the same patient cohort (n=77 NSCLC patients). Using PCA, Leiden unsupervised clustering, XGBoost classifiers, and SHAP-based feature attribution, they identified baseline liver function markers (particularly AST) and on-treatment neutrophil dynamics as the most influential features associated with durable clinical benefit — meaning the patient remained alive and progression-free at six months post-treatment. 
 
---
 
## Figures & Images
 
*Figures and specific detials are not reproduced here as the manuscript is being prepared for submission.*
 
---

## My takeaways
Leading this project was challenging as coordinating between a clinical collaborator, a faculty team, and five peers while also being responsible for a technically open-ended piece of the work pushed me in ways I didn't fully anticipate. The LLM extraction component taught me that getting reliable, consistent outputs from language models in a clinical context is much harder than it sounds, and that how you evaluate those outputs matters just as much as how you prompt for them. This project also demonstrated how AI models and prompt engineering techniques can be used to transform unstructured data into structured, machine-readable information that can support downstream research and predictive modeling. More broadly, it showed me that the value of AI in research may not always come from making predictions directly, but from enabling researchers to efficiently access and analyze information that would otherwise remain obscure. As AI continues to be integrated across biomedical research, clinical practice, and even traditional wet-lab workflows, I believe it is important to understand both the capabilities and limitations of these tools and how they can be applied responsibly to accelerate scientific discovery and this project helped me realize those capabilities. 
