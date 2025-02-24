# Financial Term Extraction using Machine Learning

## 📌 Project Overview
This project focuses on financial term extraction using machine learning techniques, specifically targeting financial documents in English and Kazakh. The dataset was obtained from the [Official Information Source managed by the Prime Minister of the Republic of Kazakhstan](https://primeminister.kz/en/news/kazakhstan-gdp-growth-of-33-in-7-months-3175939#:~:text=Official%20Information%20Source%20of%20the%20Prime%20minister%0Aof%20the%20Republic%20of%20Kazakhstan,-Version%20for%20the) and consists of financial texts with tagged terms.

## 🚀 Features
- **Financial Term Extraction**: Uses regular expressions to identify terms within `<finance>...</finance>` (English) and `<қаржы>...</қаржы>` (Kazakh) tags.
- **Machine Learning Models**: Implements XGBoost and BERT-based classification for text analysis.
- **Text Preprocessing**:
  - `CountVectorizer` for XGBoost input transformation.
  - `BERT Tokenizer` for BERT-based classification.
- **Dataset Processing**: Frequency distribution analysis of extracted terms.

## 📂 Dataset
The dataset consists of financial documents in English and Kazakh, annotated with specific tags for term extraction. The source of the dataset can be found [here](https://primeminister.kz/en/news/kazakhstan-gdp-growth-of-33-in-7-months-3175939#:~:text=Official%20Information%20Source%20of%20the%20Prime%20minister%0Aof%20the%20Republic%20of%20Kazakhstan,-Version%20for%20the).

## 🛠️ Installation
### Prerequisites
Ensure you have Python installed along with the required dependencies.

```
pip install -r requirements.txt
```

## 📊 Model Training & Evaluation
### 1. Preprocessing the Dataset
```python
from preprocessing import preprocess_data
preprocessed_data = preprocess_data("data/financial_dataset.csv")
```

### 2. Training XGBoost Model
```python
from models import train_xgboost
model_xgb = train_xgboost(preprocessed_data)
```

### 3. Training BERT Model
```python
from models import train_bert
model_bert = train_bert(preprocessed_data)
```

## 🏆 Results
- **XGBoost Classifier**: Trained using an 80/20 train-test split.
- **BERT-based Classifier**: Fine-tuned on the dataset for better term recognition.

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`feature-branch`).
3. Commit your changes.
4. Push to the branch and submit a pull request.
