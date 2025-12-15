# 🧬 Genetik Algoritma ile Numune Karışımı Optimizasyonu

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

Bu proje, **Yapay Zeka Sistemleri** dersi kapsamında geliştirilmiş bir optimizasyon projesidir. **Senaryo 7** baz alınarak, bir biyoteknoloji laboratuvarındaki test çözeltilerinin en verimli karışım oranları **Genetik Algoritma (GA)** kullanılarak hesaplanmıştır.

---

## 👨‍💻 Öğrenci Bilgileri

| **Ad Soyad** | **Okul No** | **Bölüm** |
|:---:|:---:|:---:|
| Emrah Horsunlu | 2012729007 | Bilgisayar Mühendisliği |

---

## 📌 Problem Tanımı (Senaryo 7)

Bir biyoteknoloji firması, test hassasiyetini maksimize etmek için iki reaktifin (A ve B) ideal karışım oranlarını aramaktadır.

### 📐 Matematiksel Model
**Amaç Fonksiyonu (Maximize):**
$$y = 3x_1 + 2x_2 + x_1x_2 - 0.5x_2^2$$

**Değişkenler:**
* **$x_1$**: Reaktif A Oranı (%)
* **$x_2$**: Reaktif B Oranı (%)

**Kısıtlar:**
1.  **Toplam Kısıtı:** $x_1 + x_2 \le 100$ (Toplam karışım %100'ü geçemez)
2.  **Alt Sınır:** $x_1 \ge 25$ (Reaktif A en az %25 olmalıdır)

---

## ⚙️ Kullanılan Yöntem ve Teknoloji

Proje **Python** dilinde geliştirilmiş olup, çözüm için evrimsel hesaplama tekniği olan **Genetik Algoritma** kullanılmıştır.

### Algoritma Parametreleri
* **Popülasyon Büyüklüğü:** 100 Birey
* **Jenerasyon Sayısı:** 100
* **Seçim Yöntemi:** Turnuva Seçimi (Tournament Selection)
* **Çaprazlama (Crossover):** Aritmetik Çaprazlama
* **Mutasyon:** Rastgele Değer Değişimi (Oran: 0.2)
* **Ceza Yöntemi (Penalty):** Kısıtları (Toplam > 100) ihlal eden bireylerin fitness puanı düşürülerek elenmesi sağlanmıştır.

### 📚 Kullanılan Kütüphaneler
* `NumPy` & `Pandas`: Veri işleme ve hesaplama.
* `Matplotlib` & `Seaborn`: 2D ve 3D görselleştirme.
* `Tqdm`: Algoritma ilerleme çubuğu (Progress bar).

---

## 📊 Proje Çıktıları ve Görselleştirme

Algoritma çalıştırıldığında, problem uzayını tarayarak global maksimum noktasına yakınsar. Aşağıda projenin çalışma anından alınan sonuç paneli görülmektedir:

![Simülasyon Sonuçları](sonuc_ekrani.png)

### Elde Edilen En İyi Sonuçlar:
Simülasyon sonucunda algoritma şu değerlere yakınsamıştır:

| Parametre | Bulunan Değer (%) | Açıklama |
|---|---|---|
| **Reaktif A ($x_1$)** | **%66.81** | Alt sınır kısıtına uygun |
| **Reaktif B ($x_2$)** | **%33.16** | Optimize edilmiş değer |
| **Toplam Karışım** | **%99.97** | $x_1 + x_2 \le 100$ kısıtı sağlandı |
| **Maksimum Skor** | **1932.25** | Test Hassasiyeti (Maximize Edildi) |

---

## 🚀 Kurulum ve Çalıştırma (Google Colab)

Bu proje bulut tabanlı **Google Colab** üzerinde çalıştırılmak üzere tasarlanmıştır.

1.  Repodaki `.ipynb` dosyasını indirin veya açın.
2.  Google Colab'e yükleyin.
3.  Tüm hücreleri sırasıyla çalıştırın (`Runtime` > `Run all`).
4.  Sonuç dashboard'u en alt hücrede otomatik olarak belirecektir.

---

Bu proje [Emrah Horsunlu](https://github.com/emrahhorsunlu) tarafından hazırlanmıştır.
