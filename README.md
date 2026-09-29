# Machine Learning for User Localization and Region Classification in 6G Near-Field Systems

Bu proje, **6G Near-Field (Fresnel Region) iletişim sistemlerinde makine öğrenmesi kullanarak kullanıcı konumlandırması ve yayılım bölgesi sınıflandırması** üzerine geliştirilmiştir.

Çalışmada, **0.3 THz Sub-THz frekansında Extremely Large Antenna Array (ELAA)** tabanlı sentetik bir veri seti kullanılmıştır. Amaç, Near-Field iletişim ortamındaki fiziksel özelliklerden yararlanarak kullanıcının konumunu tahmin etmek ve bulunduğu yayılım rejimini sınıflandırmaktır.

<img width="1500" height="1500" alt="kullanici_haritasi" src="https://github.com/user-attachments/assets/3a699f34-2924-473c-bd81-e22c04057c24" />


## 🎯 Projenin Amacı

6G iletişim sistemlerinde yüksek frekanslar ve çok büyük anten dizileri, kullanıcıların konum bilgilerinin daha hassas şekilde çıkarılmasına olanak sağlayabilir.

Bu çalışmada iki temel makine öğrenmesi problemi ele alınmaktadır:

* **Kullanıcı konumlandırması:** Kullanıcının mesafe ve açı bilgilerinin tahmin edilmesi
* **Bölge sınıflandırması:** Kullanıcının bulunduğu yayılım bölgesinin sınıflandırılması

Bu yaklaşım, gelecekte **yüksek hassasiyetli konumlandırma, beamforming, kaynak tahsisi ve akıllı iletişim sistemleri** gibi uygulamalarda kullanılabilecek makine öğrenmesi tabanlı yöntemlerin araştırılmasına yönelik bir temel oluşturmaktadır.

## 📊 Veri Seti

Çalışmada yaklaşık **200.000 örnek ve 31 özellikten** oluşan sentetik bir Near-Field/Fresnel veri seti kullanılmıştır.

Veri setindeki önemli değişkenlerden bazıları:

| Özellik         | Açıklama                       |
| --------------- | ------------------------------ |
| `Dist_True`     | Gerçek kullanıcı mesafesi      |
| `Angle_True`    | Gerçek kullanıcı açısı         |
| `SNR_dB`        | Sinyal-gürültü oranı           |
| `Rayleigh_Dist` | Rayleigh mesafesi              |
| `CSI_Real_Mid`  | CSI gerçek bileşeni            |
| `CSI_Imag_Mid`  | CSI sanal bileşeni             |
| `Phase_Slope`   | Faz eğimi                      |
| `path_loss`     | Yol kaybı ile ilişkili özellik |

`Dist_True` yaklaşık **0.5–50** aralığında, `Angle_True` ise yaklaşık **−1.57 ile 1.57** aralığında değerler içermektedir.

## 🧠 Kullanılan Yaklaşım

Proje kapsamında genel olarak aşağıdaki makine öğrenmesi süreci izlenmiştir:

1. Veri setinin incelenmesi
2. Eksik ve tutarsız verilerin kontrol edilmesi
3. Özelliklerin analiz edilmesi
4. Hedef değişkenlerin belirlenmesi
5. Veri ön işleme
6. Eğitim ve test verilerinin hazırlanması
7. Makine öğrenmesi modellerinin oluşturulması
8. Model performanslarının değerlendirilmesi
9. Sonuçların analiz edilmesi

### Problem 1 — Localization

Kullanıcının konumuna ilişkin sürekli değerlerin tahmin edilmesi bir **regresyon problemi** olarak ele alınmaktadır.

Özellikle:

* `Dist_True` → mesafe tahmini
* `Angle_True` → açı tahmini

üzerinden kullanıcı konumunun çıkarılması amaçlanmaktadır.

### Problem 2 — Region Classification

Kullanıcının bulunduğu yayılım rejiminin belirlenmesi ise bir **sınıflandırma problemi** olarak ele alınmaktadır.

Bu problemde modelin farklı yayılım bölgelerini ayırt edebilmesi hedeflenmektedir.

## 🔬 Teknolojiler

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook
* Machine Learning
* Data Analysis & Visualization

## 📈 Değerlendirme

Regresyon modellerinin performansı uygun hata metrikleri üzerinden, sınıflandırma modellerinin performansı ise sınıflandırma metrikleri üzerinden değerlendirilmektedir.

Kullanılan değerlendirme yaklaşımı, modelin yalnızca eğitim verisindeki başarısını değil, daha önce görmediği veriler üzerindeki genelleme performansını da incelemeye odaklanmaktadır.

## 🤖 AI Kullanımı

Projenin geliştirilme sürecinde yapay zekâ; araştırma, teknik konuların anlaşılması, kodlama sırasında karşılaşılan problemlerin analiz edilmesi, hata ayıklama ve alternatif çözüm yaklaşımlarının değerlendirilmesi amacıyla kullanılmıştır.

AI tarafından önerilen çözümler doğrudan kullanılmak yerine, **dokümantasyon ve deneysel testlerle doğrulanarak** projeye dahil edilmiştir.

## 📁 Proje Yapısı

```text
NearField-6G/
│
├── data/
│   └── ...
│
├── notebooks/
│   └── ...
│
├── src/
│   └── ...
│
├── README.md
└── requirements.txt
```

> Proje yapısı, repository içerisindeki gerçek klasörlere göre güncellenebilir.

## 🚀 Gelecek Çalışmalar

* Farklı makine öğrenmesi modellerinin karşılaştırılması
* Hiperparametre optimizasyonu
* Daha gelişmiş konumlandırma modellerinin araştırılması
* Derin öğrenme tabanlı yaklaşımların denenmesi
* Gerçek veya daha gerçekçi kanal verileriyle modelin test edilmesi
* Localization ve classification problemlerinin birlikte ele alınması

## 👩🏻‍💻 Author

**Rümeysa Elvanoğlu**

Computer Engineer | MSc Student

İlgi alanları:

* Artificial Intelligence
* Machine Learning
* 6G Communication Systems
* Software Development
* AI-Native Product Development
