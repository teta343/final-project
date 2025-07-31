# US Agriculture Analysis (2023)

![Power BI Visualization Example](https://img.shields.io/badge/Power_BI-Visualization-yellow) ![Python](https://img.shields.io/badge/Python-3.10-blue) ![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3.0-orange) ![Pandas](https://img.shields.io/badge/Pandas-2.1.4-green)

A data analysis project examining 2023 US crop production patterns using machine learning and Power BI visualization.

## 📌 Project Overview

**Sector**: Agriculture  
**Focus**: Crop production analysis in the United States  
**Problem Statement**: "Analyzing patterns in US agricultural land use to identify which crops dominate production areas and predict future trends in crop cultivation."

## 📂 Dataset

- **Source**: FAOSTAT US Crop Production 2023
- **Records**: 90 crops
- **Key Columns**:
  - `Item`: Crop name (e.g., "Maize", "Soybeans")
  - `Value`: Harvested area in hectares
  - `Size_Category`: Small/Medium/Large classification
  - `Cluster_Name`: Production level (Low/Medium/High)

## 🔍 Key Findings

### Crop Production Distribution
- **Top Dominant Crops**: Maize, Soybeans, Wheat
- **Production Categories**:
  - Large (>100k ha): 33.7% of crops
  - Medium (10k-100k ha): 40.4% of crops
  - Small (<10k ha): 25.9% of crops

![](./final-project/crop%20category.png)

### Machine Learning Insights
- Optimal clustering identified 3 production groups:
  1. Low-Production (Specialty crops like ginger, taro)
  2. Medium-Production (Commercial crops like blueberries)
  3. High-Production (Staple crops like maize)

![Cluster Visualization](screenshots/cluster_visualization.png)

## 🔧 Technical Implementation

### Data Processing Pipeline
1. **Data Cleaning**:
   - Handled missing values in harvested area metrics
   - Converted data types for numerical analysis
   - Created size categories based on hectare thresholds

2. **Feature Engineering**:
   - Applied log transformation for skewed data
   - Standardized values for clustering
   - Generated percentage contribution metrics

### Machine Learning Models
- **Unsupervised Learning**:
  - K-Means Clustering (k=3) with silhouette score of 0.55
  - Elbow method validation for optimal cluster count

- **Supervised Learning**:
  - Random Forest Classifier achieved 100% accuracy
  - SHAP values for model interpretability

![SHAP Analysis](screenshots/shap_analysis.png)

## 📊 Power BI Integration

Prepared dataset with calculated metrics for visualization:
- Cluster assignments
- Value percentages
- Size categories

![Power BI Dashboard](screenshots/powerbi_dashboard.png)

## 🚀 How to Use

1. **Data Preparation**:
   - Run the data processing notebook (`finalproject.ipynb`)
   - Output generates `Agriculture_Data_For_PowerBI.csv`

2. **Visualization**:
   - Import CSV into Power BI
   - Create dashboards with production metrics

3. **Model Deployment**:
   - Use trained models to classify new crop data
   - Predict production scale for planning purposes

## 📈 Business Applications

1. **Agricultural Planning**:
   - Identify crops with expansion potential
   - Allocate resources based on production scale

2. **Policy Recommendations**:
   - Large crops: Focus on efficiency improvements
   - Small crops: Target high-value markets

3. **Market Analysis**:
   - Correlate production scale with economic value
   - Identify niche opportunities

## 📝 Project Structure



## 🗂 Directory Details

### 1. Data Management
- **/data/raw**: Original datasets (never modified)
- **/data/processed**: Cleaned versions ready for analysis
- Key Files:
  - `FAOSTAT_data_en_7-30-2025.csv`: Source dataset from FAO
  - `Agriculture_Data_For_PowerBI.csv`: Processed output for visualization

### 2. Analysis Notebooks
- **/notebooks**: Sequential Jupyter notebooks
  - `1_data_cleaning.ipynb`: Missing value handling and transformations
  - `2_eda.ipynb`: Exploratory Data Analysis with visualizations
  - `3_clustering.ipynb`: K-Means implementation and evaluation
  - `4_prediction.ipynb`: Random Forest classification model

### 3. Output Deliverables
- **/reports/figures**: Key visualizations
  - Distribution plots
  - Cluster analysis charts
  - SHAP value diagrams
- **presentation.pdf**: Final compiled report

### 4. Supporting Files
- **/docs**: Technical documentation
  - Data dictionary explaining all variables
  - Methodology details for reproducibility
- **/environment**: Dependency specifications
  - Both pip and conda environment files

## ♻️ Workflow Process

1. **Data Ingestion**
   - Load raw data from `/data/raw`
   - Preserve original files

2. **Data Processing**
   - Clean and transform in notebooks
   - Save processed data to `/data/processed`

3. **Analysis**
   - Perform EDA and modeling
   - Save visualizations to `/reports/figures`

4. **Reporting**
   - Generate final presentation
   - Update documentation

## 🔄 Version Control
- All raw data is read-only
- Processed data regenerated from notebooks
- Notebooks show complete analysis history
