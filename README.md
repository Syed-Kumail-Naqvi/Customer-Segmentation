# Customer Segmentation Analysis

**A comprehensive K-Means clustering project for customer segmentation in retail**

---

## Project Overview

This project uses **K-Means Clustering** to segment mall customers into distinct groups based on their purchasing behavior and demographics. By analyzing customer data, we identify 5 key customer segments that enable targeted marketing strategies and personalized business approaches.

Live-Project Link: https://customer-segmentation-frontend-phi.vercel.app

**Key Objective:** Segment customers using Age, Annual Income, and Spending Score to drive targeted marketing strategies.

---

## Business Objectives

1. **Identify Customer Segments** - Discover natural groupings in customer behavior
2. **Profile Each Segment** - Understand demographics and spending patterns for each group
3. **Enable Targeted Marketing** - Create personalized strategies for each customer segment
4. **Optimize Resources** - Allocate marketing budgets to high-value segments
5. **Support Decision Making** - Provide data-driven insights for business strategy

---

## Dataset Overview

**Source:** Mall Customer Dataset  
**Records:** 200 customers  
**Features:**
- **Customer ID** - Unique identifier
- **Age** - Customer age in years
- **Gender** - Male or Female
- **Annual Income** - Annual income in thousands (k$)
- **Spending Score** - Customer spending score (0-100)

### Data Statistics:
```
Age:              18-89 years
Annual Income:    $15k - $137k
Spending Score:   1-99 (1-100 scale)
Gender Split:     ~50% Male, ~50% Female
```

---

## Analysis Components

### 1. **Exploratory Data Analysis (EDA)**
- Dataset shape and structure analysis
- Missing value and duplicate detection
- Statistical summaries (mean, std, min, max)
- Distribution visualizations for Age, Income, and Spending Score
- Gender distribution analysis
- Correlation analysis between features

### 2. **Data Preprocessing**
- Feature selection: Annual Income & Spending Score
- StandardScaler normalization for fair clustering
- Data validation and quality checks

### 3. **K-Means Clustering**
- Elbow Method to find optimal k (determined k=5)
- StandardScaler preprocessing for normalization
- Model fitting and cluster assignment
- Centroid calculation and interpretation

### 4. **Segment Profiling**
Detailed analysis of each cluster including:
- Cluster size and composition
- Average age, income, and spending score
- Gender distribution per segment
- Business characteristics and insights

---

## Customer Segments

### **Segment 0: Conservative Customers**
- Lower spending despite good income
- Target Strategy: Value-focused messaging, bundle deals
- Marketing Focus: Reliability and long-term value

### **Segment 1: Low Budget Customers**
- Low income and low spending capacity
- Target Strategy: Budget-friendly options, payment plans
- Marketing Focus: Affordability and accessibility

### **Segment 2: High Value Customers** 
- High income AND high spending (Premium segment)
- Target Strategy: Premium products, loyalty programs, VIP treatment
- Marketing Focus: Exclusivity and premium services

### **Segment 3: Potential Customers**
- Low income but high spending (Growth potential)
- Target Strategy: Income growth initiatives, up-sell opportunities
- Marketing Focus: Value-adds and investment opportunities

### **Segment 4: Impulsive Customers**
- Moderate income with very high spending
- Target Strategy: Limited-time offers, exclusive deals, flash sales
- Marketing Focus: Excitement and urgency

---

## Technologies & Libraries

**Language:** Python 3.x

**Core Libraries:**
- **pandas** - Data manipulation and analysis
- **numpy** - Numerical computing
- **scikit-learn** - Machine learning (K-Means clustering, StandardScaler)
- **matplotlib** - Data visualization
- **seaborn** - Statistical data visualization

**Additional Features:**
- Jupyter Notebook for interactive analysis
- StandardScaler for feature normalization
- KMeans for unsupervised clustering
- silhouette_score for cluster evaluation

---

## Project Structure

```
Customer-Segmentation/
├── README.md                    # Project documentation
├── requirements.txt             # Python dependencies
├── data/
│   ├── raw/
│   │   └── Mall_Customer.csv   # Original dataset
│   └── processed/              # Processed data (optional)
└── notebooks/
    └── main.ipynb              # Main analysis notebook
```

---

## Getting Started

### Prerequisites
- Python 3.7 or higher
- Jupyter Notebook

### Installation

1. **Clone/Navigate to the project:**
```bash
cd Customer-Segmentation
```

2. **Install dependencies:**
```bash
pip install -r requirements.txt
```

3. **Launch Jupyter Notebook:**
```bash
jupyter notebook
```

4. **Open and run `notebooks/main.ipynb`**

---

## Key Findings & Insights

### Clustering Results:
- **Optimal Clusters:** 5 (determined via Elbow Method)
- **Features Used:** Annual Income, Spending Score
- **Algorithm:** K-Means with StandardScaler normalization

### Customer Distribution:
- Each segment has distinct income and spending characteristics
- Gender distribution varies across segments
- Age ranges provide additional demographic insights

### Business Implications:
- High Value Segment (2) should receive premium service focus
- Potential Segment (3) represents growth opportunity
- Conservative Segment (0) values reliability over features
- Impulsive Segment (4) responds well to time-limited offers

---

## Visualizations Included

Histograms - Age, Income, and Spending Score distributions  
Donut Charts - Gender distribution (overall and by cluster)  
Bar Charts - Average metrics by cluster (Age, Income, Spending)  
Scatter Plots - Relationships between features (colored by other attributes)  
Elbow Curve - Optimal cluster determination  
Cluster Visualization - 2D plot showing segment separation  
Cluster Size Distribution - Bar chart of customer counts per segment  

---

## Workflow Summary

1. Load and explore the Mall Customer dataset
2. Perform EDA with visualizations
3. Preprocess data (standardization)
4. Apply Elbow Method to find optimal k
5. Fit K-Means model with k=5
6. Generate cluster assignments
7. Profile and analyze each segment
8. Create visualizations for business insights
9. Generate summary statistics and recommendations

---

## Key Techniques Used

- **Exploratory Data Analysis (EDA)** - Understanding data distributions and relationships
- **Data Standardization** - StandardScaler for feature normalization
- **Elbow Method** - Determining optimal number of clusters
- **K-Means Clustering** - Unsupervised learning algorithm
- **Data Visualization** - Matplotlib and Seaborn for insights
- **Cluster Profiling** - Comprehensive segment analysis

---

## Learning Outcomes

By studying this project, you'll learn:
- How to perform customer segmentation using K-Means
- Techniques for choosing optimal cluster numbers
- Data preprocessing and standardization best practices
- How to profile and interpret customer segments
- Creating professional data visualizations
- Translating ML results into business insights

---

## Notes & Considerations

- The dataset contains 200 customer records from a mall
- K-Means was chosen for its simplicity and interpretability
- Elbow Method suggested k=5 as optimal
- StandardScaler ensures features with different ranges are treated equally
- Results are highly interpretable for business decision-making

---

## Future Enhancements

- Include Age in clustering features for more nuanced segmentation
- Implement hierarchical clustering for comparison
- Add silhouette score and other evaluation metrics
- Create interactive dashboards for segment exploration
- Build predictive models for new customer segment assignment
- Add RFM (Recency, Frequency, Monetary) analysis
- Incorporate customer lifetime value (CLV) metrics

---

## Contact & Support

For questions or suggestions regarding this project, feel free to reach out.

---

**Last Updated:** April 2026  
**Status:** Complete and Ready for Production
│   └── main.ipynb # Main Jupyter Notebook
├── data/
│   ├── raw/
│   │   └── Mall_Customers.csv          # Original dataset
│   └── processed/                       # (For future use)
├── requirements.txt                     # Python dependencies
└── README.md                            # This file
```

---

## Dataset

**Source:** Mall_Customers.csv

**Features:**
- **CustomerID** - Unique customer identifier
- **Gender** - Customer gender (Male/Female)
- **Age** - Age of the customer (years)
- **Annual Income (k$)** - Annual income in thousands of dollars
- **Spending Score (1-100)** - Score assigned based on spending behavior (1-100)

**Dataset Size:** 200 customers × 5 features

---

## Technical Stack

### Libraries Used:
- **pandas** - Data manipulation and analysis
- **numpy** - Numerical computations
- **matplotlib** - Data visualization
- **seaborn** - Statistical data visualization
- **scikit-learn** - Machine learning (K-Means, StandardScaler)

### Installation:
```bash
pip install -r requirements.txt
```

---

## How to Run

### Run Jupyter Notebook (Recommended)
```bash
jupyter notebook notebooks/main.ipynb
```

---

## Analysis Steps

### 1. **Data Loading & Preprocessing**
   - Load customer data from CSV
   - Check for missing values and duplicates
   - Generate statistical summary
   - Prepare data for clustering

### 2. **Data Visualization**
   - **Histograms**: Age, Income, Spending Score distributions
   - **Donut Chart**: Gender split
   - **Bar Charts**: Average metrics by gender
   - **Scatter Plots**: Relationships between features

### 3. **Feature Scaling**
   - Standardize features using StandardScaler
   - Ensure equal importance for all features in clustering

### 4. **Find Optimal Clusters (Elbow Method)**
   - Test k values from 2 to 10
   - Calculate inertia for each k
   - Identify the "elbow point"
   - **Result:** Optimal k = 5 clusters

### 5. **Apply K-Means Clustering**
   - Train K-Means model with k=5
   - Assign customers to clusters
   - Calculate cluster centroids

### 6. **Cluster Profiling**
   - Analyze characteristics of each segment
   - Calculate average age, income, spending score per cluster
   - Determine gender distribution

---

## Customer Segments Identified

### 1. **Conservative Customers**
- **Size:** ~35 customers
- **Characteristics:**
  - Good/High income
  - Low spending score
  - Careful with money despite having purchasing power
- **Marketing Strategy:** Focus on value and quality

### 2. **Low Budget Customers**
- **Size:** ~35 customers
- **Characteristics:**
  - Low income
  - Low spending score
  - Limited purchasing power
- **Marketing Strategy:** Budget-friendly options, payment plans

### 3. **High Value Customers** 
- **Size:** ~40 customers
- **Characteristics:**
  - High income
  - High spending score
  - Premium segment with strong purchasing power
- **Marketing Strategy:** Premium products, loyalty rewards, exclusive offers

### 4. **Potential Customers**
- **Size:** ~44 customers
- **Characteristics:**
  - Low income
  - High spending score
  - High engagement despite limited income
- **Marketing Strategy:** Income growth programs, up-sell opportunities

### 5. **Impulsive Customers**
- **Size:** ~46 customers
- **Characteristics:**
  - Moderate income
  - Very high spending score
  - Spontaneous buyers
- **Marketing Strategy:** Limited-time offers, flash sales, exclusive deals

---

## Key Visualizations

The notebook includes the following charts (each in a separate cell):

1. **Histograms** - Distribution of Age, Income, Spending Score
2. **Donut Chart** - Gender distribution
3. **Bar Charts** - Average metrics by gender and by cluster
4. **Scatter Plots** - Relationships between features (colored by different metrics)
5. **Cluster Visualization** - Main result showing 5 customer segments
6. **Cluster Profiling** - Characteristics of each segment

---

## K-Means Algorithm Details

### How it Works:
1. **Initialization** - Randomly select k initial centroids
2. **Assignment** - Assign each point to nearest centroid
3. **Update** - Recalculate centroid positions based on assigned points
4. **Repeat** - Continue until centroids don't change significantly

### Optimal k = 5
- Determined using **Elbow Method**
- Balance between model complexity and performance
- Clear, interpretable segments

---

## Business Recommendations

### For Each Segment:

| Segment | Strategy | Action Items |
|---------|----------|--------------|
| **High Value** | Premium Experience | VIP program, exclusive access, personalized service |
| **Potential** | Growth Initiative | Career development content, income growth programs |
| **Impulsive** | Maximize Engagement | Flash sales, trending products, limited offers |
| **Conservative** | Value Messaging | Quality focus, investment perspective |
| **Low Budget** | Accessibility | Entry-level products, installment plans, discounts |

### Overall Strategy:
- Tailor marketing messages to each segment
- Allocate marketing budget based on segment value
- Design products/services for each segment
- Improve customer lifetime value through targeted retention

---

## Results & Insights

### Cluster Distribution:
- Relatively balanced distribution across 5 segments
- No single dominant segment
- Opportunity in all customer categories

### Key Findings:
- Strong differentiation between segments
- Clear behavioral patterns based on income and spending
- Gender is relatively balanced across segments
- Age varies within clusters (demographic independence)

---

## Model Performance

- **Algorithm:** K-Means Clustering
- **Number of Clusters:** 5
- **Features Used:** Income, Spending Score
- **Scaling Method:** StandardScaler
- **Random State:** 42 (for reproducibility)

---

## Files Description

### `main.ipynb`
- Interactive Jupyter Notebook
- Cell-by-cell visualization (each chart separate)
- Comprehensive exploratory analysis
- Perfect for presentations and learning
- Includes detailed insights and interpretations

---

## 🎓 Learning Outcomes

After completing this project, you will understand:

How to load and preprocess customer data  
How to apply K-Means clustering algorithm  
How to determine optimal number of clusters (Elbow Method)  
How to interpret and profile customer segments  
How to create professional data visualizations  
How to translate ML results into business insights  

---

## Related Concepts

- **Unsupervised Learning** - K-Means is an unsupervised algorithm
- **Feature Scaling** - Importance of standardization in clustering
- **Exploratory Data Analysis (EDA)** - Understanding data before modeling
- **Customer Analytics** - Using ML for business intelligence

---

## References

### K-Means Clustering:
- [Scikit-learn KMeans Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html)
- [Wikipedia - K-Means Clustering](https://en.wikipedia.org/wiki/K-means_clustering)

### Data Visualization:
- [Matplotlib Documentation](https://matplotlib.org/)
- [Seaborn Documentation](https://seaborn.pydata.org/)

### Data Analysis:
- [Pandas Documentation](https://pandas.pydata.org/)
- [NumPy Documentation](https://numpy.org/)

---

## Author

**Syed Kumail Naqvi, Muhammad Wasaf and Usman Jamal**  
2nd Year Data Science Group Project  
Customer Segmentation with K-Means Clustering

---

## License

This project is created for educational purposes as part of 2nd year coursework.

---

## Notes

- K-Means is sensitive to feature scaling (already handled)
- Results are reproducible with random_state=42
- Visualizations are optimized for presentation
- Each notebook cell can be run independently

---

**Last Updated:** April 28, 2026
