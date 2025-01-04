# Makine Öğrenmesi ile İnme Tahmini

## Proje Açıklaması
Bu proje, hastaların cinsiyet, yaş, tıbbi geçmiş ve sigara kullanımı gibi özelliklerine dayanarak inme geçirme olasılığını tahmin etmeyi amaçlamaktadır. Kullanılan veri seti, bağımlı değişken olan `stroke` (inme) ile birlikte 7 bağımsız değişkenden oluşmaktadır. Veri setinde görülen sınıf dengesizliği SMOTE gibi yöntemlerle dengelenmiş, modeller hiperparametre optimizasyonları ile geliştirilmiştir.


---

## Veri Seti
- **Kaynak**: CSV dosyası (309 KB)
- **Hedef Değişken**: `stroke` (ikili sınıflandırma - inme geçirme durumu)
- **Temel Özellikler**:
  - Eksik `bmi` değerleri ortalama ile dolduruldu.
  - Özellikler normalizasyon ve standardizasyon ile ölçeklendirildi.

---

## Veri Ön İşleme
1. **Eksik Verilerin Doldurulması**: `bmi` sütunundaki eksik değerler ortalama ile dolduruldu.
2. **Ölçeklendirme**:
   - `age`, `bmi`, ve `avg_glucose_level` için standardizasyon.
   - `avg_glucose_level` için normalizasyon.
3. **Önemli Özelliklerin Seçilmesi**: Korelasyon analizi ve Recursive Feature Elimination (RFE) yöntemleri kullanıldı.

---

## Kullanılan Modeller
- **K-Nearest Neighbors (KNN)**
- **Destek Vektör Makineleri (SVM)**
- **Lojistik Regresyon**
- **Karar Ağaçları**

### Hiperparametre Optimizasyonu
- Hiperparametre optimizasyonu için **GridSearchCV** kullanılmıştır.
- KNN ve Karar Ağacı modellerinde görülen aşırı öğrenme problemleri parametre ayarlarıyla çözüldü.

---

## Sonuçlar
- SVM, doğruluk, kesinlik, duyarlılık ve F1 skorlarında diğer modelleri geride bırakmıştır.
- KNN modeli için GridSearchCV yetersiz kalmış, manuel parametre ayarları yapılmıştır.

---

## Çalıştırma Adımları
1. Depoyu klonlayın:  
   ```bash
   git clone <repository_link>
   cd <repository_name>

# Stroke Prediction Using Machine Learning Models

## Project Description
This project aims to predict the likelihood of a stroke based on various patient attributes such as gender, age, medical history, and smoking habits. The dataset used for this purpose includes 7 independent variables and 1 dependent variable (`stroke`), with a significant class imbalance. The team tackled the imbalance using techniques like SMOTE and optimized the models through hyperparameter tuning.


---

## Dataset
- **Source**: CSV file (309 KB)
- **Target Variable**: `stroke` (binary classification - stroke occurrence)
- **Key Features**:
  - Missing `bmi` values were filled using the mean.
  - Features scaled via normalization and standardization.

---

## Data Preprocessing
1. **Handling Missing Data**: Filled missing `bmi` values with the mean.
2. **Scaling**:
   - Standardization applied to `age`, `bmi`, and `avg_glucose_level`.
   - Normalization applied to `avg_glucose_level`.
3. **Feature Selection**: Used correlation analysis and Recursive Feature Elimination (RFE).

---

## Models Used
- **K-Nearest Neighbors (KNN)**
- **Support Vector Machines (SVM)**
- **Logistic Regression**
- **Decision Tree Classifier**

### Hyperparameter Tuning
- **GridSearchCV** was employed for hyperparameter optimization. 
- Issues like overfitting in KNN and Decision Tree models were mitigated by adjusting hyperparameters.

---

## Results
- SVM outperformed other models in terms of accuracy, precision, recall, and F1 score.
- KNN required manual parameter adjustments due to GridSearchCV limitations.

---

## How to Run
1. Clone the repository:  
   ```bash
   git clone <repository_link>
   cd <repository_name>   
