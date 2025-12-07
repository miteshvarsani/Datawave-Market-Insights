# Datawave-Music-User-Analytics

This project analyses user behaviour, churn patterns, pricing sensitivities, and demographic trends of **Datawave Music**, an online music subscription platform. The aim is to identify growth opportunities, understand churn drivers, and outline actionable recommendations that can support market expansion and improve customer retention.

This analysis was completed as part of the **Institute of Analytics (IOA) – Autumn Student Sprint Challenge 2025**.  
Tools used: **Power BI**, **Python (KNN Imputer + Clustering)**, **Excel & Power Query**.

---

## Project Overview

Datawave Music provided a dataset capturing user registrations, subscription types, demographics, listening behaviour, skip rates, satisfaction ratings, churn status, and pricing.  
The aim of this project was to deliver key insights around:

- Registration trends  
- Age-based segmentation  
- Churn drivers  
- Pricing sensitivity  
- Market performance  
- Customer churn (causes)  
- Growth opportunities  

---

## Data Quality & Cleaning

The raw dataset contained multiple inconsistencies that required extensive cleaning across Excel, Power Query, and Python.

### Data Quality Issues Identified
- Missing values in **Gender**, **Satisfaction Score**, and **Monthly Fee**
- Duplicate User IDs  
- Blank User IDs  
- Mis-spelled or inconsistent country names and subscription types  
- Mixed date formats (MM/DD vs DD/MM)  
- Skip Rate stored as percentages, decimals, and whole numbers  
- Monthly Fee values not matching subscription tier  
- Mixed churn values (0/1 vs Yes/No)

### Cleaning Steps
- Standardised skip rate and subscription types  
- Fixed date issues using `try_otherwise` logic in Power Query  
- Standardised churn to Yes/No  
- Applied KNN Imputer (after Ordinal Encoding + Scaling) to fill missing values  
- Created new IDs for users with blank IDs using country + age + gender  
- Removed duplicates  
- Exported cleaned file for dashboarding in Power BI  

---

## Dashboard & Files


The interactive dashboard can be downloaded via the link included on the GitHub page.

---

## 🔍 Key Insights

### 1. Registrations Trend
- Overall registrations have been **declining** across most markets.  
- **Nigeria and South Africa** are exceptions, showing **an upward trend** in new sign-ups.  
- However, these two growth markets also have the **lowest satisfaction scores** (2.82 and 2.93), which may threaten long-term retention.  

---

### 2. Subscriber Age Market Analysis
- In the **USA**, users aged **30+** make up the majority, suggesting a gap in younger audiences.  
- Surprisingly, **66% of student-plan subscribers are aged 30+**, indicating misuse of discounted plans and potential revenue leakage.  
- Users aged **41–45** and **60+** have the **longest listening hours**, contradicting assumptions that youth are the heaviest consumers.  
- Opportunity: Create **youth-focused content and marketing**, especially in Western markets.

---

### 3. Metrics Leading to Higher Churn
- Churn peaks sharply after **474 songs played**.  
- Users within the **470–490** song range represent the **highest churn risk**.  
- Price sensitivity is extremely high:
  - Plans priced at **12.99** show the **highest churn**.
  - Plans priced at **5.00** perform very well and could be leveraged for student or promotional pricing.
- Opportunity: Introducing exclusive offers and discounts to customers between their 470th to 490th song can help improve retention
  
---

### 4. Churn Analysis Across Markets
- **India, USA, Nepal** show the **lowest churn**, indicating stable markets.  
  However, registrations are still falling — suggesting retention is strong but acquisition is weakening.  
- **Brazil** has the **highest churn (38.46%)**, yet its users have the **longest listening hours** (11.72 hours on average).  
  This indicates a deeply engaged user base that could be reactivated and used for testimonials or localised campaigns.  
- In many regions (Brazil, Kenya, Nepal, UK, USA), **churned users gave higher ratings than active users**, indicating dissatisfaction among current customers.

---

## 🗺 Market-Specific Insights

### Nigeria & South Africa  
- Fastest-growing markets for registrations  
- Also the lowest satisfaction ratings. This calls for urgent need for CX improvements  

### Brazil  
- High churn but extremely engaged listeners  
- Opportunity: push Brazilian artists, localised playlists, and targeted re-engagement campaigns  

### USA & Nepal  
- Low churn but declining registrations  
- Marketing efforts should shift towards new user acquisition  

### India & Kenya  
- Free-plan users show the lowest churn  
- High potential for converting free users to paid subscriptions  

---

## ✔️ Recommendations

### Platform-Wide Recommendations
1. **Standardise pricing** across subscription types. Currently different prices are charged for the same subscription types. Standardising this can help create clarity.
2. **Restrict student plans** to users under 30 to prevent misuse.  
3. Introduce **retention offers** for users who are between their **470th–490th song**.  
4. Review the **12.99 pricing tier** — consider reducing the maximum price to **9.99**.  
5. Launch **customer feedback surveys** to understand dissatisfaction drivers.  

### Market-Specific Recommendations
1. Extend Nigeria & SA’s growth strategies to declining markets.  
2. Improve service quality in markets with low ratings (Nigeria & SA).  
3. Create youth-focused content and campaigns in USA + Europe.  
4. Analyse Brazilian listening habits and collaborate with local artists.  
5. Gather additional data from India, Nepal, and USA to understand why churn is low.

---

## 🛠 Tools & Technologies Used

- **Power BI** – Dashboarding  
- **Python** – KNN Imputation, Clustering, Preprocessing  
- **Excel / Power Query** – Initial data transformations  
- **Pandas & Scikit-Learn** – Pipeline development  

---

