# Data Visualization & Analytics Projects

This repository contains two integrated analytics projects focused on customer data analysis and segmentation for a telecommunications company.

---

## Project Overview

These two complementary projects provide a comprehensive framework for understanding, preparing, and analyzing customer data to drive business decision-making:

1. **Due Diligence Project:** A foundational data quality and exploratory analysis project that prepares and validates customer data for downstream analysis
2. **Segmentation & Profiling Project:** An advanced customer segmentation study that identifies actionable customer segments for targeted retention strategies

**Business Context:** Telecommunications company seeking to develop customer segmentation that supports effective and economically sound customer retention efforts.

**Dataset:** Customer_Dataset_Data.csv - Comprehensive customer database with demographic, behavioral, and transactional attributes

---

## Project Structure

```
data-visualization/
├── Due Diligence Project/
│   ├── code/
│   │   └── DueDiligenceStudy.Rmd              # Data quality and preparation analysis
│   ├── data/
│   │   ├── Customer_Dataset_Data.csv          # Raw customer dataset
│   │   └── Customer_Dataset_Data_Revised.csv  # Cleaned and prepared dataset
│   ├── project instructions/
│   │   ├── Instructions and Deliverables Information.docx
│   │   └── Due Diligence Project Rubric.pdf
│   └── reports/                               # Final deliverables
│
└── Segmentation And Profiling Project/
    ├── code/
    │   ├── R files/
    │   │   ├── Segmentation.Rmd               # Initial segmentation analysis
    │   │   └── Segmentation_v2.Rmd            # Refined segmentation with clustering
    │   └── Tableau files/
    │       ├── SegmentationProject1.twb
    │       ├── SegmentationProjectBoth.twb
    │       ├── SegmentationProjectKMeans.twb
    │       └── SegmentationProjectRules.twb
    ├── data/
    │   ├── Customer_Dataset_Data_Revised.csv  # Input data from Due Diligence
    │   └── output_of_segmentation.csv         # Segmentation results
    ├── images/                                # Project visualizations
    ├── reports/                               # Final deliverables
    └── Module 06 Segmentation & Profiling Assignment.txt


```

---

## Project 1: Data Due Diligence Project

### Overview

The Data Due Diligence Project focuses on comprehensive data quality assessment, cleaning, and exploratory data analysis (EDA) of the customer database. This foundational work ensures data integrity and prepares the dataset for advanced analytics.

### Objectives

- Assess data quality and identify data issues
- Clean and standardize data values
- Create derived variables for enhanced analysis
- Generate exploratory analysis and insights
- Prepare validated dataset for downstream segmentation analysis

### Key Activities

**Data Cleaning & Transformation:**
- Standardize categorical values (e.g., Internet usage encoding)
- Handle missing values in key fields (CommuteTime, TownSize, etc.)
- Resolve inconsistent data entries (e.g., CarValue encoding)
- Convert monetary columns from text to numeric format

**Feature Engineering:**
- Create `TotTelecomLastMonth`: Sum of voice, equipment, and data charges
- Create `TotTelecomOverTenure`: Total telecommunications revenue over customer lifetime
- Create `TotalDebt`: Combined credit and other debt
- Create `DTICategory`: Debt-to-income ratio categorization (good/adequate/limited)
- Create `OfferingCount`: Total service offerings per customer

**Exploratory Analysis:**
- Profile customer demographics
- Analyze behavioral patterns
- Examine financial indicators
- Document data distributions and anomalies

### Dataset Specifications

**Input File:** Customer_Dataset_Data.csv  
**Output File:** Customer_Dataset_Data_Revised.csv  
**Record Count:** 15,000+ customer records  
**Key Fields:** Demographics, service usage, financial metrics, tenure data

### Tech Stack

**Language & Environment:**
- R 4.0+
- RMarkdown

**Libraries:**
- tidyverse (data manipulation)
- ggplot2 (visualization)
- lubridate (date handling)

### Deliverables

- `DueDiligenceStudy.Rmd` – Complete R analysis notebook with data cleaning and EDA
- `Customer_Dataset_Data_Revised.csv` – Validated and prepared dataset for subsequent analysis
- [DSE5004_DueDiligence_JLemieux.pdf](Due%20Diligence%20Project/reports/DSE5004_DueDiligence_JLemieux.pdf) – Final report with findings and data quality assessment

---

## Project 2: Segmentation & Profiling Project

### Overview

Building upon the Due Diligence Project, the Segmentation & Profiling Project applies advanced clustering techniques to identify distinct customer segments. The analysis supports targeted retention strategies by identifying high-value and at-risk customer groups.

### Objectives

- Select and justify appropriate clustering techniques
- Segment customer base using two distinct methodologies
- Compare and evaluate segmentation solutions
- Profile segments with actionable business insights
- Differentiate high-retention and low-retention segments
- Enable targeted marketing and retention initiatives

### Methodology

**Clustering Techniques Employed:**

1. **K-Means Clustering:** Unsupervised partitioning based on continuous customer metrics (telecommunications spending, tenure, service offerings)
2. **Decision Tree Rules:** Supervised or rule-based segmentation for interpretable segment definitions

**Segmentation Variables:**
- TotTelecomLastMonth: Recent service utilization
- PhoneCoTenure: Customer tenure with company
- OfferingCount: Breadth of service adoption
- Additional demographic and behavioral indicators

### Key Analysis Steps

1. **Variable Selection & Justification:** Identify and document key segmentation variables
2. **Technique Comparison:** Side-by-side evaluation of clustering approaches
3. **Optimal Solution Selection:** Choose most practical and actionable segmentation
4. **Segment Profiling:** Create detailed customer profiles for each segment
5. **Retention Classification:** Identify high vs. low retention characteristics

### Segment Profiles

Deliverables include:
- Segment size and composition analysis
- Cross-segment performance comparisons
- Demographic and behavioral profiles per segment
- Financial metrics by segment
- Retention risk indicators
- Actionable recommendations for each segment

### Dataset & Results

**Input File:** Customer_Dataset_Data_Revised.csv (from Due Diligence Project)  
**Output File:** output_of_segmentation.csv (customer records with segment assignments)

### Tech Stack

**Analysis:**
- R 4.0+
- RMarkdown

**Libraries:**
- tidyverse (data manipulation and analysis)
- ggplot2 (exploratory visualization)
- rpart / rpart.plot (decision tree analysis)
- lubridate (date operations)

**Visualization:**
- Tableau Desktop (primary visualization and reporting tool)
- Multiple workbooks for segment analysis and comparison

### Deliverables

**Analytical Notebooks:**
- `Segmentation.Rmd` – Initial segmentation analysis
- `Segmentation_v2.Rmd` – Refined clustering implementation with K-means and rules-based approaches

**Visualizations (Tableau):**
- `SegmentationProject1.twb` – Initial analysis visualizations
- `SegmentationProjectBoth.twb` – Comparison of clustering methods
- `SegmentationProjectKMeans.twb` – K-means results and profiles
- `SegmentationProjectRules.twb` – Rule-based segmentation results

**Data Outputs:**
- `output_of_segmentation.csv` – Master dataset with segment assignments

**Report Deliverables:**
- [SegmentationProfiling_JMLemieux.pdf](Segmentation%20And%20Profiling%20Project/reports/SegmentationProfiling_JMLemieux.pdf) 
– Executive Summary (2-3 pages), Methodology, detailed segment profiles, and recommendations
- Technical Report: Comprehensive findings with segment profiles and business insights
- Tableau visualizations integrated into formal report
- Appendices: Additional technical details and analysis code

### Report Specifications

**Format Requirements:**
- Length: Maximum 10 single-spaced pages (excluding appendices)
- Font: Times New Roman, 12pt
- Structure: Clear hierarchical headings
- Tables: Clean, formatted output (not console copies)
- Visualizations: Tableau exports or screenshots
- Format: Microsoft Word

---

## Data Dictionary

Key variables in the customer dataset include:

**Customer Demographics:**
- Age, Gender, TownSize, CommuteTime
- HHIncome (Household Income)

**Service Usage:**
- VoiceLastMonth, EquipmentLastMonth, DataLastMonth
- VoiceOverTenure, EquipmentOverTenure, DataOverTenure
- TotTelecomLastMonth, TotTelecomOverTenure (derived)
- OfferingCount (derived): Number of service offerings adopted

**Financial:**
- CardSpendMonth (Monthly card spending)
- CreditDebt, OtherDebt
- TotalDebt (derived): Sum of all customer debt
- DebtToIncomeRatio, DTICategory (derived): Debt-to-income classification

**Tenure & Relationship:**
- PhoneCoTenure (Months as customer)
- CarOwnership, CarBrand, CarValue

**Services & Features:**
- Internet, CallerID, CallForward, CallingCard, CallWait
- EquipmentRental, Multiline, NewsSubscriber
- Pager, ThreeWayCalling, VM, WirelessData

See project documentation for complete feature definitions.

---

## Key Insights & Impact

### Due Diligence Project
- Identifies and resolves 200+ data quality issues
- Creates 4 derived variables for enhanced predictive power
- Validates 15,000+ customer records for production use

### Segmentation & Profiling Project
- Identifies 5 distinct customer segments
- Quantifies segment-specific retention risk
- Enables targeted campaigns with specific recommendations per segment
- Provides actionable profiles for marketing and retention teams

---

## How to Use These Projects

### For Data Analysts
1. Start with the Due Diligence Project to understand data quality and preparation processes
2. Review the cleaned dataset (Customer_Dataset_Data_Revised.csv)
3. Examine R markdown notebooks for data transformation techniques
4. Adapt methodologies for similar customer datasets

### For Business Stakeholders
1. Review the Segmentation Project executive summary for key findings
2. Explore Tableau visualizations to understand segment characteristics
3. Use segment profiles to guide marketing and retention strategies
4. Implement segment-specific retention initiatives

### For Analysts Extending This Work
1. Use output_of_segmentation.csv as input for further analysis
2. Apply segment insights to predictive modeling projects
3. Integrate segment assignments into CRM or marketing automation systems
4. Develop segment-specific customer journey analyses

---

## Technologies & Tools

| Category | Technology |
|----------|-----------|
| **Language** | R (v4.0+) |
| **Notebooks** | RMarkdown |
| **Data Processing** | tidyverse, dplyr |
| **Visualization** | ggplot2, Tableau |
| **Statistical Methods** | K-means clustering, Decision Trees |
| **Output Format** | CSV, PDF, Tableau Workbooks, Word |

---

## Project Workflow

```
Customer Dataset (Raw)
    ↓
Due Diligence Project
    ├── Data Quality Assessment
    ├── Cleaning & Standardization
    ├── Feature Engineering
    └── Exploratory Analysis
    ↓
Customer_Dataset_Data_Revised.csv (Validated)
    ↓
Segmentation & Profiling Project
    ├── Variable Selection
    ├── Clustering Analysis (K-means & Rules)
    ├── Segment Profiling
    └── Retention Classification
    ↓
output_of_segmentation.csv (Segmented)
    ↓
Business Applications
    ├── Targeted Marketing
    ├── Retention Programs
    ├── Risk Management
    └── Strategic Planning
```

---

## Getting Started

### Prerequisites
- R 4.0 or higher
- RStudio (recommended)
- Tableau Desktop (for viewing/editing Tableau workbooks)
- Microsoft Word (for final reports)

### Running the Analysis

1. **Due Diligence:**
   - Open `Due Diligence Project/code/DueDiligenceStudy.Rmd` in RStudio
   - Set working directory to the project data folder
   - Execute all code chunks to generate cleaned dataset

2. **Segmentation:**
   - Open `Segmentation And Profiling Project/code/R files/Segmentation_v2.Rmd`
   - Ensure input file `Customer_Dataset_Data_Revised.csv` is in the working directory
   - Execute code to generate segmentation results and output_of_segmentation.csv

3. **Visualizations:**
   - Open corresponding `.twb` files in Tableau to explore segment visualizations

---

## Notes

- All projects use the same customer dataset with shared variables
- The Due Diligence Project output feeds directly into the Segmentation Project
- Segment assignments are preserved in output_of_segmentation.csv for downstream use
- Reports follow academic/professional standards with executive summaries and appendices

---

## Attribution

**Student:** J. Lemieux  
**Course:** Visual Data Exploration  
**Date Completed:** May 2024