# SVM-Based Copy Number Caller for Human Genomes

## Project Overview
This project aims to develop a machine learning model using Support Vector Machine (SVM) for calling Copy Number Variations (CNVs) in human genomes. CNVs, significant in genetic research and medicine, involve segments of the genome that have been either deleted or duplicated. Accurate detection and classification of CNVs are crucial for understanding genetic variations, diagnosing genetic diseases, and advancing personalized medicine.

### Objective
- **Primary Goal**: Develop an SVM model to efficiently and accurately identify CNVs from genomic data.
- **Significance**: Enhance the understanding of genetic variations and contribute to the field of genetic disorder diagnosis and personalized medicine.
- **Performance Criteria**: The model must demonstrate high accuracy, precision, recall, and F1-score.

## Data Loading and Preprocessing
- **Data Sources**: Genomic markers indicative of CNVs, using 10 genomes from the Human Pangenome Research Consortium.
- **Ground Truth**: A hidden Markov model based CNV caller (`hmcnc`) provided the ground truth set for training.
- **Initial Processing**: Libraries such as `csv`, `numpy`, `pandas`, `matplotlib.pyplot`, `seaborn`, and `joblib` were used for data manipulation and visualization.
- **Feature Engineering**:
  - Encoding chromosome numbers and aggregating data for meaningful feature formation.
  - Expanding certain columns to capture nuanced information indicative of CNVs.
- **Data Transformation**:
  - Scaling features for optimal SVM performance.

## Data Exploration and Visualization
- **PCA Visualization**: Applied to understand variance in high-dimensional data.
- **t-SNE and UMAP Visualization**: Used for observing clustering patterns in genomic data.

## Model Implementation
- **Model Choice**: SVM with RBF kernel.
- **Data Splitting**: Dataset divided into training and test sets.
- **Cross-Validation**: Employed Stratified K-Fold cross-validation for reliable performance assessment.

## Performance Evaluation
- **Training**: The SVM model distinguishes between two classes: '0' (neutral copy state) and '1' (deletion or duplication).
- **Evaluation Metrics**: Accuracy, precision, recall, and F1-score.

## Results and Insights
- **Test Set Evaluation**:
  - Accuracy: ~98.97%.
  - Precision and Recall: Nearly perfect for Class 0 (Normal), high for Class 1 (Variant).
  - F1-Score: Strong balance between precision and recall.
- **Independent Test Set Evaluation**: Consistent performance, highlighting the model's robustness and generalizability.
- **Cross-Validation**: Average accuracy, precision, recall, and F1 score at 99%.

## Conclusion
The SVM model demonstrates exceptional capability in identifying CNVs, showing high accuracy and reliability. This project contributes significantly to genomic studies, particularly in the accurate detection of CNVs.

## Future Work
- Further optimization and validation on larger datasets.
- Exploration of additional features and alternative machine learning models for comparison.

