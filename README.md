Machine-Learning-with-Brain-Tumor-Dataset-Classification-and-Clustering-Model

# Brain Tumor Classification & Clustering Project

## Proje Açıklaması
Bu proje, beyin tümörü teşhisi için hem gözetimli hem de gözetimsiz makine öğrenmesi algoritmalarını kullanarak bir sınıflandırma ve kümeleme modeli oluşturmayı amaçlar. Veriseti, bir dizi **ilk-ölçekli** ve **ikinci-ölçekli** özellikten oluşur ve sınıf etiketi tümör varlığı (1) veya yokluğu (0) ile tanımlanır.

## Veri Seti
Veriseti beyin tümörlerinin sınıflandırılması için kullanılan 13 özelliği içermektedir:

- **İlk-Ölçekli Özellikler**:
  - Mean
  - Variance
  - Standard Deviation
  - Skewness
  - Kurtosis

- **İkinci-Ölçekli Özellikler**:
  - Contrast
  - Energy
  - ASM (Angular Second Moment)
  - Entropy
  - Homogeneity
  - Dissimilarity
  - Correlation
  - Coarseness

Sınıf etiketi (Class): 
- `1`: Tümör var
- `0`: Tümör yok

## Kullanılan Algoritmalar
1. **Gözetimli Öğrenme (Supervised Learning)**:
   - Logistic Regression: Tümör sınıflandırması için kullanıldı. Model, test verisindeki performansı değerlendirmek için `accuracy`, `precision`, `recall`, ve `f1-score` gibi metriklerle analiz edildi.
  
2. **Gözetimsiz Öğrenme (Unsupervised Learning)**:
   - K-Means Clustering: Görüntüler, tümör var veya yok olarak iki kümeye ayrıldı ve özellikler arasında doğal ayrım analiz edildi.

## Proje Adımları
1. **Veri Hazırlama**:
   - Veriler yüklenip incelendi ve eksik veriler temizlendi.
   - Sınıf ve görüntü sütunları, model eğitimi için ayrıldı.

2. **Gözetimli Model: Logistic Regression**:
   - Model eğitildi ve test verisinde performansı değerlendirildi.
   - Sonuçlar karışıklık matrisi (confusion matrix) ve sınıflandırma raporu ile görselleştirildi.

3. **Gözetimsiz Model: K-Means**:
   - 2 küme belirlendi ve veriler kümelere ayrıldı.
   - Kümeler görselleştirildi ve merkez noktaları işaretlendi.

## Sonuçlar
- **Logistic Regression** modelinin doğruluk oranı oldukça başarılıydı ve beyin tümörü tespiti için güvenilir sonuçlar verdi.
- **K-Means Clustering**, sınıflar arasında belirgin bir ayrım olup olmadığını ortaya koydu, ancak kümeleme sonuçları sınıflandırma kadar başarılı değildi. Yine de, ham veri analizi ve ayrımların incelenmesi açısından yararlı oldu.

## Gereksinimler
Projeyi çalıştırmak için aşağıdaki kütüphaneler gereklidir:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
