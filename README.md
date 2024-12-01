## K-Nearest Neighbors (KNN) Classification with Custom and Scikit-learn Models

Implemented the K-Nearest Neighbors (KNN) classification algorithm using both a custom implementation and the `scikit-learn` library. 
The project includes various datasets, including the **Hayes-Roth**, **Car Evaluation**, and **Breast Cancer** datasets, to evaluate and compare the performance of both models.

### Key Steps Taken:

1. **Data Preprocessing**:
   - For each dataset, data was read and preprocessed to fit the format suitable for machine learning tasks.
   - Categorical data was encoded using `LabelEncoder()` to convert non-numeric values into numeric format, as required for the KNN algorithm.
   
2. **Custom KNN Implementation**:
   - A custom KNN classifier was implemented, including:
     - Different distance metrics for neighbor calculation: **Euclidean**, **Manhattan**, and **Hamming** distances.
     - A weighted voting mechanism for classification where closer neighbors have more influence on the prediction.
     - Cross-validation (K-Fold) to evaluate model performance. The training data was split into `numFolds` to ensure that each data point was used for both training and testing,
       improving the model's generalization ability.
       
3. **Performance Evaluation**:
   - For each distance metric (`Euclidean`, `Manhattan`, and `Hamming`), the mean accuracy of both the custom and `scikit-learn` KNN classifiers was computed.
   - The performance was evaluated in terms of accuracy, where the mean accuracies of both models were compared across the different datasets.

4. **Scikit-learn KNN**:
   - The `scikit-learn` KNN classifier was also used to perform classification on the same datasets, allowing for a direct comparison of results with the custom implementation.
   - This step involved training the model using the same datasets and evaluating the performance with multiple distance metrics.

5. **K-Fold Cross Validation**:
   - The K-Fold cross-validation technique was used to ensure a fair evaluation by splitting the data into multiple subsets (folds).
   - The model was trained and tested on each fold, and performance metrics were calculated.
   - The results were stored and compared across different distance metrics and the two KNN implementations (custom vs. `scikit-learn`).

6. **Hypothesis Testing**:
   - Paired sample t-tests were performed to assess whether there was a significant difference between the custom KNN and `scikit-learn` models for each distance metric.
   - The null hypothesis was tested, where a p-value greater than 0.05 would lead to the acceptance of no significant difference between the two models,
     and a p-value less than 0.05 would indicate a significant difference.
     
### Conclusion:

The implementation provided insights into the working of the KNN algorithm and how different distance metrics influence model performance.
It also helped compare the custom implementation with the more efficient and optimized `scikit-learn` version. 
The hypothesis tests further validated the accuracy results, determining if the differences observed were statistically significant.


