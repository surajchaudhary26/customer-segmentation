# customer-segmentation# Customer Churn Clustering using KMeans

This project performs **customer segmentation** using the **KMeans clustering algorithm** on a customer churn dataset. The objective is to group customers into clusters based on behavioral and service usage patterns.

---

## 📂 Dataset

- **Source**: `customer_churn.csv`
- **Records**: 7043
- **Features**: 21
- Features include:
  - `gender`, `SeniorCitizen`, `Partner`, `Dependents`, `tenure`, `PhoneService`, `InternetService`, etc.
  - Target variable: `Churn` (used for understanding customer behavior, but not in unsupervised learning)

---

## 🧰 Libraries Used

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `sklearn` (KMeans, LabelEncoder, StandardScaler)

---

## 🔍 Project Workflow

1. **Importing Dependencies**
2. **Loading the Dataset** from CSV
3. **Initial Exploration**:
   - `df.head()`, `df.info()`, `df.shape`
   - Check for null values and duplicates
4. **Data Preprocessing**:
   - Label Encoding categorical columns
   - Drop `customerID` (not useful for clustering)
   - Optional: Standardize the dataset (commented out in the code)
5. **Clustering using KMeans**:
   - Create a model with `n_clusters=3`
   - Fit the model and assign labels to data
   - Add `Clusters` column to original dataframe
6. **Finding Optimal Clusters**:
   - Use the **Elbow Method** to plot **Sum of Squared Distances (SSD)** for `k` in range [2, 10]
   - Helps to visually choose the best number of clusters

---

## 📊 Output

- Clusters are added to the dataframe.
- Boxplots are used to analyze outliers in numerical columns.
- Elbow curve is plotted to determine optimal clusters.

---

## ✅ Future Improvements

- Apply feature scaling (`StandardScaler`) before KMeans for better results.
- Use dimensionality reduction techniques like **PCA** for visualization.
- Evaluate clusters using silhouette score or other clustering metrics.
- Try different clustering algorithms like **DBSCAN** or **Agglomerative Clustering**.

---

## 📎 Usage

Run the Jupyter Notebook or Google Colab file step-by-step to reproduce the clustering and visualization.

---

## 📧 Contact

For any queries or suggestions, feel free to reach out.

