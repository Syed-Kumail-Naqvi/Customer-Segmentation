# Customer Segmentation Analysis
## K-Means Clustering Project

---

## Project Overview

This project implements **Customer Segmentation** using K-Means clustering to group customers into meaningful segments based on their behavior and characteristics. It demonstrates how machine learning can be used to identify distinct customer groups for targeted marketing strategies.

**Objective:** Group customers into meaningful segments based on:
- Age
- Annual Income
- Spending Score

---

## Key Insights

### Segment Interpretations:

1. **Conservative Customers** - Lower spending despite having good income
2. **Low Budget Customers** - Low income and low spending
3. **High Value Customers** - High income AND high spending (Premium segment)
4. **Potential Customers** - Low income but high spending (Growth potential)
5. **Impulsive Customers** - Moderate income with very high spending

### Business Recommendations:
- **Target High Value**: Premium products and loyalty programs
- **Focus on Potential**: Income growth initiatives, up-sell opportunities
- **Engage Impulsive**: Limited-time offers, exclusive deals
- **Develop Conservative**: Value-focused messaging
- **Support Low Budget**: Budget-friendly options, payment plans

---

## Project Goals

1. **Load & Explore Data** - Understand customer demographics and purchasing patterns
2. **Apply K-Means Clustering** - Group customers using the K-Means algorithm
3. **Find Optimal Clusters** - Use Elbow Method to determine the best number of clusters
4. **Profile Segments** - Analyze characteristics of each customer segment
5. **Visualize Results** - Present findings with clear, professional visualizations

---

## Project Structure

```
Customer-Segmentation/
├── notebooks/                          
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