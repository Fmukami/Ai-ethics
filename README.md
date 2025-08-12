# Ai-ethics
# Part 1: Theoretical Understanding 
1. Short Answer Questions
Q1: Define algorithmic bias and provide two examples of how it manifests in AI systems.

Answer:
Algorithmic bias refers to systematic and repeatable errors in a computer system that create unfair outcomes, such as privileging one group over others.
Example 1: An AI recruiting tool trained on resumes mainly from male candidates may favor male applicants, disadvantaging women.
Example 2: A facial recognition system that is less accurate for people with darker skin tones, leading to higher misidentification rates for minorities.

Q2: Explain the difference between transparency and explainability in AI. Why are both important?
Answer:
Transparency means making the inner workings and decision processes of an AI system open and accessible, such as disclosing data sources and model architectures.
Explainability is the ability to interpret and understand the AI’s decisions or predictions, often by providing reasons or logic behind outputs.
Both are important because transparency builds trust and accountability, while explainability allows stakeholders to understand, challenge, and appropriately use AI decisions, especially in sensitive domains.

Q3: How does GDPR (General Data Protection Regulation) impact AI development in the EU?

Answer:
GDPR requires organizations to protect personal data and privacy, impacting AI by mandating data minimization, user consent, and the right to explanation for automated decisions. AI systems must be designed to allow users to access, rectify, and erase their data, and explain how automated decisions are made, ensuring accountability and user rights.

2. Ethical Principles Matching
Match the following principles to their definitions:

Principle	Definition
A) Justice	Fair distribution of AI benefits and risks
B) Non-maleficence	Ensuring AI does not harm individuals or society.
C) Autonomy	Respecting users’ right to control their data and decisions.
D) Sustainability	Designing AI to be environmentally friendly.

# Part 2: Case Study Analysis 
Case 1: Biased Hiring Tool
Source of Bias:

The bias originated from training data: The system was trained on resumes submitted over a decade, mostly by men, causing it to learn male-dominated patterns and penalize resumes with female-associated terms.
Three Fixes:

Balanced Training Data: Re-train the model on a gender-balanced dataset.
Feature Auditing: Remove gendered terms or proxies for gender from the feature set.
Bias Mitigation Algorithms: Apply fairness constraints or debiasing techniques such as reweighting or adversarial debiasing during model training.
Fairness Metrics:

Disparate Impact Ratio: Measures selection rate across genders.
Equal Opportunity Difference: Difference in true positive rates between genders.
Demographic Parity: The outcome should be independent of gender.


Case 2: Facial Recognition in Policing
Ethical Risks:

Wrongful arrests due to misidentification, particularly of minorities.
Privacy violations from surveillance and tracking.
Erosion of public trust in law enforcement and technology.
Reinforcement of systemic biases against marginalized groups.
Policy Recommendations:

Rigorous third-party audits for accuracy and bias before deployment.
Human-in-the-loop verification for all matches; no arrests based solely on AI output.
Clear consent and notification policies for use in public spaces.
Transparency and public reporting of system performance and error rates by demographic group.
Part 3: Practical Audit (25%)
Sample Python Code Using AI Fairness 360

aif360_compas_audit.py
import pandas as pd
from aif360.datasets import CompasDataset
from aif360.metrics import BinaryLabelDatasetMetric, ClassificationMetric
import matplotlib.pyplot as plt

# Load COMPAS data
Sample Report (Approx. 300 words)

compas_audit_report.md
# COMPAS Dataset Bias Audit Report

**Objective:**  
To audit the COMPAS recidivism dataset for racial bias using the AI Fairness 360 toolkit, focusing on disparities in false positive rates between demographic groups.

**Methods:**  
Part 4: Ethical Reflection (5%)
Prompt: Reflect on a personal project (past or future). How will you ensure it adheres to ethical AI principles?

Sample Response:
In a recent natural language chatbot project, I ensured ethical AI by anonymizing user data, seeking user consent for data use, and regularly auditing outputs for offensive or biased content. Moving forward, I will incorporate fairness metrics, maintain transparency about how user data is used, and provide users with avenues to challenge or opt out of automated decisions, ensuring respect for autonomy, justice, and non-maleficence.

Bonus Task
Policy Proposal: 1-Page Guideline for Ethical AI Use in Healthcare

ethical_ai_healthcare_guideline.md
# Ethical AI Use in Healthcare: Guidelines

## 1. Patient Consent Protocols
- Obtain explicit, informed consent from patients before collecting or using personal health data for AI purposes.
- Clearly explain the purpose, risks, and benefits of AI-driven decisions to patients.
- Allow patients to withdraw consent and request deletion of their data at any time.
  ## 2. Bias Mitigation Strategies
- Routinely audit training data and model outputs for demographic biases (e.g., race, gender, age).
- Employ fairness-aware algorithms and rebalancing techniques to reduce disparities.
- Involve diverse stakeholders, including clinicians and patient representatives, in model validation.

## 3. Transparency Requirements
- Disclose the use of AI in clinical workflows to patients and staff.
- Provide clear, accessible explanations of AI-driven decisions, including limitations and sources of error.
- Maintain documentation on data sources, model development, validation results, and updates.

## 4. Accountability and Governance
- Designate responsible parties for monitoring AI system performance and addressing adverse events.
- Establish procedures for reporting, investigating, and resolving potential harm caused by AI systems.
- Regularly review guidelines and update them in light of new evidence or technologies.

## 5. Security and Privacy
- Apply robust security measures to protect patient data used by AI systems.
- Comply with applicable regulations (e.g., GDPR, HIPAA) regarding data protection and patient rights.
