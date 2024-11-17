<p align="center">
    <img src="https://github.com/user-attachments/assets/9d0e8c97-d484-40e8-9e29-f6008639f853" alt="malicious banner" height="400">
</p>

# Malicious Link Detection

The proposed machine learning model uses a Random Forest classifier to classify URLs as `malicious` or `benign`. The model focuses on analyzing a variety of features derived from the URL itself, such as structural attributes (e.g., URL length, number of special characters, or the presence of IP addresses) and lexical patterns.

By leveraging these features, the Random Forest algorithm builds an ensemble of decision trees to make accurate and reliable predictions, helping to identify potentially harmful links efficiently

## Kaggle Dataset
[Malicious links](https://www.kaggle.com/datasets/sid321axn/malicious-urls-dataset)

A dataset containing 651,191 URLs, out of which 428103 benign or safe URLs, 96457 defacement URLs, 94111 phishing URLs, and 32520 malware URLs

## Approach
- Combined defacement, phishing and malware classes to a single class malicious
- Wrote several functions to extract features from just the URLs
- Used sklearn's BaseEstimators and TransformerMixin to construct pipelines
- After preprocessing, used RandomForestClassifier to detect the malicious URLs

## Challenges

- I encountered a significant class imbalance due to the limited number of defacement, phishing, and malware URLs. Adjusting class weights alone did not yield satisfactory results. As a solution, I consolidated all these categories into a single "malicious" category.
- Neural Networks, even after extensive hyperparameter tuning, achieved a maximum accuracy of 81%. To improve performance, I transitioned to a Random Forest Classifier, which significantly outperformed with an accuracy of 95%.

## Performance

- **F-1 Score** : 95%

## Links 🖇️:

**Kaggle Dataset** : [Malicious links](https://www.kaggle.com/datasets/sid321axn/malicious-urls-dataset) \
**Model** : [Malicious Link Detection Model](https://drive.google.com/file/d/1N7F3zTHSjEi_X8dsk3MG3YUyEzXFUrF1/view?usp=sharing)
