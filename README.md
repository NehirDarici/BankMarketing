# Banka Pazarlama Kampanyası - Vadeli Mevduat Tahmini 🏦📊

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Makine Öğrenmesi](https://img.shields.io/badge/Makine_Öğrenmesi-Sınıflandırma-brightgreen)

## 📌 Genel Bakış
Bu depo, bir banka müşterisinin vadeli mevduat hesabına abone olup olmayacağını tahmin etmek için tasarlanmış bir makine öğrenmesi projesini içermektedir. Sınıflandırma modeli; çeşitli müşteri demografik bilgileri, finansal geçmişler ve doğrudan pazarlama kampanyası verileri analiz edilerek oluşturulmuştur.

## 🎯 Hedefler
* Müşteri davranışlarındaki örüntüleri ortaya çıkarmak için kapsamlı bir **Keşifçi Veri Analizi (EDA)** gerçekleştirmek.
* Eksik verilerin işlenmesi, özellik ölçeklendirme (feature scaling) ve kategorik değişken kodlama (encoding) gibi **Veri Ön İşleme** tekniklerini uygulamak.
* Müşteri kararlarını doğru bir şekilde tahmin etmek ve gelecekteki pazarlama stratejilerini optimize etmeye yardımcı olmak için çeşitli **Makine Öğrenmesi Sınıflandırma Modellerini** eğitmek ve değerlendirmek.

## 📂 Veri Seti
Bu projede **Banka Pazarlama Veri Seti** (orijinal olarak UCI Makine Öğrenmesi Deposundan) kullanılmaktadır. 
* **Özellikler (Features):** Müşteri demografisi (yaş, meslek, medeni durum, eğitim), finansal göstergeler ve geçmiş kampanya etkileşimleri.
* **Hedef Değişken (Target):** `y` — Müşteri vadeli mevduata abone oldu mu? (İkili sınıflandırma: 'yes', 'no')

## 🛠️ Teknolojiler ve Kütüphaneler
* **Dil:** Python
* **Veri İşleme:** Pandas, NumPy
* **Veri Görselleştirme:** Matplotlib, Seaborn
* **Model Geliştirme:** Scikit-learn (Lojistik Regresyon, Rastgele Orman, Karar Ağaçları vb.)

## 📊 Sonuçlar ve Değerlendirme

Proje kapsamında eğitilen modeller arasında en yüksek performansı ve sınıflandırma başarısını **LightGBM** algoritması göstermiştir. Test verisi üzerinde elde edilen performans metrikleri aşağıdaki gibidir:

* **Doğruluk (Accuracy):** %90.27
* **ROC-AUC Skoru:** %92.45
* **Kesinlik (Precision):** %62.22
* **Duyarlılık (Recall):** %42.82
* **F1-Skoru:** %50.73

**Model Değerlendirmesi:**
* Modelin **%92.45 gibi oldukça yüksek bir ROC-AUC skoruna** sahip olması, algoritmanın sınıfları (abone olacaklar ve olmayacaklar) birbirinden ayırmada genel olarak çok başarılı olduğunu kanıtlamaktadır.
* **%90.27'lik genel doğruluk (accuracy)** oranı modelin güvenilirliğinin yüksek olduğunu göstermektedir.
* Banka pazarlama veri setlerinde sıklıkla karşılaşılan sınıf dengesizliği (sınırlı sayıda "evet" yanıtı olması) nedeniyle duyarlılık (recall) oranı %42.82 seviyesinde gerçekleşmiştir. Buna rağmen %62.22'lik kesinlik (precision) oranı, modelin "abone olacak" dediği müşterilerin büyük bir çoğunluğunun gerçekten teklifi kabul ettiğini göstermektedir. Bu durum, pazarlama bütçesinin doğru ve hedefli kullanılması açısından büyük bir avantaj sağlar.
