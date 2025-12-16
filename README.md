# 🧬 Genetik Algoritma ile Numune Karışımı Optimizasyonu

![Status](https://img.shields.io/badge/Durum-Tamamlandı-success) ![Python](https://img.shields.io/badge/Python-3.x-blue)

Bu proje, **Yapay Zeka Sistemleri** dersi için hazırlanmıştır. **Senaryo 7**'deki biyoteknoloji problemi, Genetik Algoritma kullanılarak modellenmiş ve çözülmüştür.

## 👨‍💻 Öğrenci Bilgileri
* **Ad Soyad:** Emrah Horsunlu
* **Öğrenci No:** 2012729007
* **Senaryo:** 7 (Numune Karışımı)

---

## 📌 Problem Tanımı
Bir laboratuvar, test hassasiyetini ($y$) maksimize etmek için iki reaktifin ($x_1, x_2$) ideal karışım oranını aramaktadır.

* **Amaç Fonksiyonu:** $y = 3x_1 + 2x_2 + x_1x_2 - 0.5x_2^2$
* **Kısıtlar:**
    1.  $x_1 + x_2 \le 100$ (Toplam %100'ü aşamaz)
    2.  $x_1 \ge 25$ (Reaktif A en az %25 olmalı)

---

## ⚙️ Kullanılan Algoritma ve Yöntemler
Projede Python dili ve aşağıdaki Genetik Algoritma bileşenleri kullanılmıştır:

1.  **Kodlama:** Gerçel Değerli Kodlama (Real-valued encoding).
2.  **Seçilim:** Turnuva Seçimi (Tournament Selection).
3.  **Çaprazlama:** Aritmetik Çaprazlama (İki genin ağırlıklı ortalaması).
4.  **Mutasyon:** Rastgele gürültü ekleme (%20 oranında).
5.  **Ceza Yöntemi (Penalty):** Kısıtları ihlal eden (toplamı 100'ü geçen) bireylere çok düşük puan verilerek elenmeleri sağlanmıştır.

---

## 📊 Sonuçlar ve Görselleştirme
Algoritma 80 jenerasyon sonunda optimum noktaya yakınsamıştır.

| Parametre | Bulunan Değer | Açıklama |
|---|---|---|
| **Reaktif A ($x_1$)** | **%66.81** | Optimize edilmiş değer |
| **Reaktif B ($x_2$)** | **%33.16** | Optimize edilmiş değer |
| **Toplam Karışım** | **%99.97** | Kısıt sağlandı ($ \le 100$) |
| **Maksimum Skor** | **1932.25** | Hedeflenen en yüksek hassasiyet |

### Grafik Analizi
Aşağıdaki grafikte algoritmanın başarımı, karışım oranları ve çözüm uzayı görülmektedir:

![Proje Çıktısı](sonuc_grafigi.png)

*(Not: Bu görseli projeyi çalıştırdıktan sonra GitHub'a yüklemelisiniz)*

---

## 🚀 Kurulum
1.  Bu repoyu klonlayın.
2.  `.ipynb` dosyasını Google Colab veya Jupyter Notebook ile açın.
3.  Tüm hücreleri çalıştırın.
