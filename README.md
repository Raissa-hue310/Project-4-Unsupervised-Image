# 🖼️ Project 4 — Unsupervised Image Clustering and Visualization  
**Business Intelligence Analyst Program – Willis College**  
**Author: Raïssa Matho Mekjele**

This project applies unsupervised machine learning techniques to the MNIST-like digits dataset using clustering and dimensionality reduction. The objective is to discover natural groupings of handwritten digit images and to visualize high-dimensional data using PCA and t-SNE.

The project demonstrates how unsupervised learning can reveal structure and patterns in image datasets without predefined labels.

---

## 📁 1. Dataset Overview

The Scikit-learn digits dataset contains:

- **1,797 images**  
- **8×8 pixel grayscale images**  
- Flattened into **64 numerical features**  
- True digit labels (*not used for clustering*)

The dataset is ideal for unsupervised clustering due to its size and structure.

---

## 🔧 2. Data Preparation & Preprocessing

Steps performed:

- Loaded the digits dataset from Scikit-learn  
- Flattened image matrices into vector form  
- Normalized data using **StandardScaler**  
- Visualized sample images  
- Analyzed label distribution (optional EDA)

Normalization was essential since pixel intensity scales vary across features.

---

## 🧩 3. K-Means Clustering

### **Elbow Method**
The elbow method was applied using k values from 2 to 15.  
The optimal number of clusters was found to be **k ≈ 10**, aligning naturally with the 10 handwritten digits.

### **Final K-Means Model**
A K-Means model with **k = 10** was trained on the scaled dataset.

### **Cluster Centroids**
Centroids were reshaped back into 8×8 images, producing **average digit templates**.

These centroid images visually represented the “prototypes” learned by each cluster, showing patterns resembling digits such as 0, 1, 5, etc.

---

## 🎯 4. Cluster Prediction on New Images

To demonstrate real-world usage:

- First 10 images from the dataset were passed to the trained K-Means model  
- Predicted cluster labels were displayed  
- Images were visualized with corresponding cluster assignments  

This shows how the clustering algorithm generalizes to unseen samples.

---

## 🎨 5. Dimensionality Reduction & Visualization

Two techniques were used:

### ⭐ **PCA (Principal Component Analysis)**  
- Reduced data to 2 components  
- Visualized clusters in a 2D scatterplot  
- Provided a coarse but useful separation of groups  

### ⭐ **t-SNE (t-Distributed Stochastic Neighbor Embedding)**  
- Captured nonlinear relationships  
- Produced highly separated, meaningful clusters  
- Clear visual grouping of handwritten digits  

t-SNE provided the best visualization of cluster structure.

---

## 🔍 6. Findings & Insights

- Clustering successfully grouped handwritten digits based on pixel similarity  
- Cluster centroids looked like averaged digit representations  
- PCA offered broad grouping while t-SNE offered much clearer separation  
- True labels (optional) showed partial alignment with clusters  
- Overlaps occurred due to variability in handwriting styles  
- Unsupervised learning proved effective for structure discovery in images  

---

## ✔ 7. Conclusion

This project demonstrated:

- Effective clustering using K-Means  
- Determination of optimal clusters using the elbow method  
- Visualization of cluster centroids as images  
- High-quality dimensionality reduction using PCA and t-SNE  
- Practical prediction of cluster labels for new image data  

Unsupervised learning provided deep insights into the dataset’s natural structure and variability.  
The results met all project requirements for clustering, visualization, and interpretation.

---

## 🛠️ 8. Tools & Libraries Used

- Python  
- NumPy  
- Pandas  
- Scikit-learn  
- Matplotlib  
- Seaborn  

---

## ✨ Author

**Raïssa Matho Mekjele**  
Business Intelligence Analyst Program  
Willis College (Ottawa)
