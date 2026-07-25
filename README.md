# RASSAD — AI-Based Compliance Monitoring System for Data Privacy under the Saudi Personal Data Protection Law (PDPL)
An AI-powered system that enables organizations in Saudi Arabia to monitor and assess their compliance with the Personal Data Protection Law (PDPL), using Natural Language Processing (NLP), deep learning, and Explainable AI (XAI).

## Project Idea

Manual PDPL compliance auditing is time-consuming, susceptible to human error, and becomes increasingly difficult to manage as the volume of data expands. This project addresses these challenges through an automated solution that:

- Automatically detects potential violations from text.
- Provides transparent explanations for each prediction, making the model's decisions understandable.
- Offers actionable recommendations to help resolve detected compliance issues based on the type of violation.

# System Components
1. Classification Module – An AI model that analyzes the input text and predicts whether it complies with PDPL by classifying it into one of 17 violation categories or "No Violation."
2. Explainable AI (XAI) Module – Employs the Integrated Gradients method from the Captum library to identify the words that contributed most to the model's prediction and associates them with the corresponding PDPL article.
3. Recommendation Module – A rule-based component that produces tailored recommendations and practical corrective actions based on the detected violation type.
4. Interactive Dashboard (Demo) – A bilingual Streamlit web application (Arabic/English) that includes Home, Compliance Check, PDPL Standards, Dashboard, and History pages. The Compliance Check page allows users to either enter text manually or upload Word, PDF, or plain text files for automated compliance analysis.

## Datasets Used

Multiple datasets were integrated and preprocessed:

- Synthetic PII Finance (Gretel.ai)
- Nemotron-PII (NVIDIA)
- PII External Dataset (Kaggle)
- Synthetic Dataset for PII Detection in Financial Documents (Mendeley)
- Official PDPL legal text
- World's Biggest Data Breaches and Hacks (Kaggle)
- GDPR Violations and Sanctions (GitHub)

# Models & Results
| Metric | DistilRoBERTa | BiLSTM | XLNet |
|--------|--------------:|--------:|-------:|
| Accuracy | 93.85% | 94.65% | 91.17% |
| F1 Score | 89.99% | 88.53% | 74.52% | 
| Precision | 93.86% | 95.00% | 90.72% | 
| Recall | 93.85% | 94.65% | 91.17% |

DistilRoBERTa was selected as the final model for achieving the best balance across classes (F1-score).

## Tech Stack
•	Python · PyTorch · Hugging Face Transformers · Captum (XAI) · Scikit-learn · Streamlit

## Demo Screenshots
Home Page 
![Home Page](https://github.com/lamabalqahtani/RASSAD-/blob/main/images/Home%20Page.jpg?raw=true)

Check Compliance, XAI Explination & Recommendations
![Check Compliance](https://github.com/lamabalqahtani/RASSAD-/blob/main/images/Check_Compliance.png?raw=true)

Users can input text directly or upload documents (Word, PDF, TXT) to evaluate compliance. The system instantly delivers compliance status, XAI explanations linked to PDPL articles, and actionable recommendations in a single view.

PDPL Standards
![PDPL Standards](https://github.com/lamabalqahtani/RASSAD-/blob/main/images/PDPL_Standards.png?raw=true)
A reference guide offering simplified explanations for each article of the Saudi Personal Data Protection Law (PDPL).
