
# Sentiment and Emotion Analysis in Indian Languages

A comprehensive machine learning project for sentiment and emotion classification in Hindi and Telugu languages using advanced NLP techniques and transformer models.

## 🎯 Project Overview

This project focuses on developing robust sentiment and emotion analysis models for Indian languages (Hindi and Telugu) using state-of-the-art NLP techniques. The system preprocesses multilingual text data, generates contextual embeddings, and applies both traditional machine learning and transformer-based models for accurate classification.

## 🗂️ Dataset

- **Languages**: Hindi and Telugu
- **Data Sources**: Multiple datasets combined for comprehensive coverage
- **Labels**: 
  - Sentiment: Positive, Negative, Neutral
  - Emotions: Joy, Sadness, Anger, Fear, Surprise, Disgust, etc.
- **Preprocessing**: Text normalization, cleaning, and standardization

## 🔧 Key Features

- **Multilingual Support**: Native processing of Hindi and Telugu text
- **Dual Classification**: Both sentiment and emotion analysis
- **Advanced Embeddings**: IndicBERT-based contextual representations
- **Multiple Models**: Traditional ML and transformer-based approaches
- **High Accuracy**: Achieved 98% sentiment and 99% emotion classification accuracy

## 🛠️ Technical Stack

### Libraries & Frameworks
```
- Python 3.8+
- TensorFlow/PyTorch
- Transformers (Hugging Face)
- scikit-learn
- pandas
- numpy
- matplotlib/seaborn
- NLTK/spaCy
```

### Models Used
- **IndicBERT** (AI4Bharat) - Primary transformer model
- **Support Vector Machine (SVM)**
- **Random Forest**
- **Custom Neural Networks**

## 📊 Project Architecture

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│   Raw Data      │───▶│   Preprocessing  │───▶│  Combined Data  │
│ Hindi + Telugu  │    │ & Normalization  │    │    Dataset      │
└─────────────────┘    └──────────────────┘    └─────────────────┘
                                                         │
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│   Evaluation    │◀───│   Model Training │◀───│   Embeddings    │
│   & Results     │    │   & Fine-tuning  │    │   Generation    │
└─────────────────┘    └──────────────────┘    └─────────────────┘
```

## 🚀 Getting Started

### Prerequisites
```bash
pip install transformers torch tensorflow scikit-learn pandas numpy matplotlib seaborn nltk
```

### Installation
```bash
git clone https://github.com/yourusername/sentiment-emotion-indian-languages.git
cd sentiment-emotion-indian-languages
pip install -r requirements.txt
```

## 📈 Methodology

### 1. Data Preprocessing
- **Text Normalization**: Standardized Unicode characters for Hindi and Telugu
- **Cleaning**: Removed noise, special characters, and irrelevant content
- **Language Detection**: Separated and processed Hindi and Telugu texts
- **Data Combination**: Merged datasets while maintaining language-specific features

### 2. Emotion Generation
- **Rule-based Labeling**: Initial emotion assignment based on lexicons
- **Manual Annotation**: Expert review for quality assurance
- **Sentence-level Analysis**: Generated emotions for individual sentences
- **Context Preservation**: Maintained semantic meaning during processing

### 3. Embedding Generation
- **IndicBERT Integration**: Used AI4Bharat's pre-trained IndicBERT model
- **Tokenization**: Applied appropriate tokenization for Hindi and Telugu text
- **Vector Representations**: Generated contextual embeddings for the combined dataset
- **Dimension Optimization**: Processed embeddings for efficient model training

### 4. Model Training

#### Traditional Machine Learning
- **SVM**: Support Vector Machine with RBF kernel
- **Random Forest**: Ensemble method with 100 estimators
- **Feature Engineering**: TF-IDF and embedding-based features

#### Transformer Model (IndicBERT)
- **Base Model**: AI4Bharat's IndicBERT
- **Fine-tuning**: Task-specific adaptation for sentiment and emotion
- **Multitask Learning**: Joint training for both classification tasks
- **Optimization**: AdamW optimizer with learning rate scheduling

## 📊 Results

### Performance Metrics

| Model | Sentiment Accuracy | Emotion Accuracy | F1-Score |
|-------|-------------------|------------------|----------|
| SVM | 85% | 82% | 0.83 |
| Random Forest | 90% | 87% | 0.88 |
| **IndicBERT (Fine-tuned)** | **98%** | **99%** | **0.98** |

### Language-wise Performance
- **Hindi**: 97% sentiment, 98% emotion accuracy
- **Telugu**: 98% sentiment, 99% emotion accuracy

## 🔍 Model Details

### IndicBERT Fine-tuning
- **Base Model**: AI4Bharat's IndicBERT for Indian languages
- **Multitask Learning**: Joint training for sentiment and emotion classification
- **Hyperparameters**: Optimized learning rate, batch size, and epochs
- **Training Strategy**: Fine-tuned on the combined Hindi-Telugu dataset

### Training Process
1. **Data Splitting**: 80% train, 10% validation, 10% test
2. **Cross-validation**: 5-fold CV for robust evaluation
3. **Hyperparameter Tuning**: Grid search for optimal parameters
4. **Early Stopping**: Prevented overfitting with patience=3

## 📁 Implementation

**Development Environment**: Google Colab
- **Single Notebook Implementation**: Complete end-to-end pipeline in one Colab file
- **GPU Acceleration**: Utilized Colab's GPU resources for model training
- **Interactive Development**: Real-time experimentation and visualization

## 🎯 Workflow

The complete pipeline was implemented in a single Google Colab notebook with the following steps:

1. **Data Loading & Preprocessing**: Imported and cleaned Hindi and Telugu datasets
2. **Data Integration**: Combined datasets while preserving language-specific characteristics  
3. **Emotion Labeling**: Generated emotion labels for sentences using rule-based and manual methods
4. **Embedding Creation**: Applied IndicBERT to generate contextual embeddings for the combined dataset
5. **Model Training**: Trained and compared SVM, Random Forest, and fine-tuned IndicBERT models
6. **Evaluation**: Assessed model performance using accuracy, F1-score, and confusion matrices
7. **Results Analysis**: Analyzed model performance across languages and emotion categories

## 🔬 Experiments & Analysis

### Ablation Studies
- **Embedding Comparison**: IndicBERT vs multilingual BERT vs Word2Vec
- **Feature Analysis**: Impact of different preprocessing techniques
- **Model Comparison**: Traditional ML vs transformer performance


## 🚧 Future Work

- [ ] **Code-mixing Support**: Handle Hindi-English and Telugu-English mixed text
- [ ] **Real-time API**: Deploy model as REST API service
- [ ] **Additional Languages**: Extend to Tamil, Bengali, Gujarati
- [ ] **Emotion Granularity**: Fine-grained emotion categories
- [ ] **Contextual Analysis**: Document-level sentiment analysis


## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **AI4Bharat** for the IndicBERT model
- **Hugging Face** for the transformers library
- **Research Community** for advancing NLP in Indian languages


## 📚 References

1. Kunchukuttan, A., et al. "IndicBERT: A pre-trained language model for Indian languages." 2020.
2. Devlin, J., et al. "BERT: Pre-training of Deep Bidirectional Transformers." 2018.
3. Various Indian language processing papers and resources.
