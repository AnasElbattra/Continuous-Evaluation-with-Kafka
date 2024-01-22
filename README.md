# Continuous Learning Project with Kafka: Cybersecurity Threat Detection

## Static Analysis

In the static phase, our project prioritized data quality through comprehensive cleansing and feature creation. Duplicate entries were meticulously removed, ensuring data integrity. Transformation of 'longest_word' and 'sld' columns using hash functions not only anonymized data but also standardized variable-length input. Statistical analysis, including skewness and histograms, provided visual insights into data distribution and patterns. The balanced dataset underwent a strategic feature selection process utilizing both f_classif and mutual_info_classif methods. This resulted in the identification of the top six features, a crucial step for subsequent machine learning model training.

### Feature Selection Details
For feature selection, the f_classif method was preferred for its ability to statistically test individual features, eliminating irrelevant ones and mitigating the risk of overfitting. Simultaneously, the mutual_info_classif method was employed to capture nonlinear relationships between features and the target, ensuring a holistic understanding.

### Model Comparison and Hyperparameter Tuning
The project employed two robust machine learning algorithms, XGBoost and Random Forest, known for their efficacy in handling cybersecurity data complexities. A thorough hyperparameter tuning process, including an exhaustive grid search, was conducted to optimize model performance. The resulting F1 scores were visualized to provide a clear comparison between baseline and tuned models.

<img src="https://github.com/AnasElbattra/Book-Recommendation-ChatBot/assets/75434006/2914dbe4-3824-4e91-a19a-97555d2945a8" alt="Bias" width="200"/>

## Dynamic Analysis

In the dynamic phase, our project embraced continuous learning principles with Kafka, focusing on real-time cybersecurity threat detection using windows of 1,000 datapoints for consumer data.

### Continuous Learning Mechanism
A transparent and effective training reevaluation process was established. Initially, the dynamic model mirrored the static model. However, to enhance the dynamic model's performance, a threshold of 0.79 was set. If the dynamic model score fell below this threshold, a retraining process was initiated, updating weights in the XGBoost model and subsequently reevaluating.

### Evaluation Metrics and Results
The static and dynamic models underwent comprehensive evaluation, utilizing the F1 score as the primary metric due to its balance between precision and recall. The results were insightful, revealing variable accuracy in the static model across different data batches. The dynamic model, updated with new data, demonstrated comparable accuracy before retraining, indicating potential benefits of continuous learning. Post-retraining, the dynamic model exhibited further improvements in accuracy.

<img src="https://github.com/AnasElbattra/Book-Recommendation-ChatBot/assets/75434006/2914dbe4-3824-4e91-a19a-97555d2945a8" alt="Bias" width="200"/>

**Advantages and Limitations:** The dynamic model, capable of retraining with new data, generally showed improved accuracy, emphasizing the benefits of integrating real-time data. However, the effectiveness of retraining varied across different data batches, emphasizing the need for robust models capable of handling diverse data landscapes. This project underscores the importance of adapting machine learning models to evolving cybersecurity challenges.

---

