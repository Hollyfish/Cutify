# Mobil Frontend Görev Dağılımı

Bu dokümanda, mobil uygulamanın kullanıcı arayüzü (UI) ve kullanıcı deneyimi (UX) görevleri listelenmektedir. Her grup üyesi, kendisine atanan ekranların tasarımı, implementasyonu ve kullanıcı etkileşimlerinden sorumludur.

---

## Grup Üyelerinin Mobil Frontend Görevleri

1. [Arda Kabay'ın Mobil Frontend Görevleri](Arda-Kabay/Arda-Kabay-Mobil-Frontend-Gorevleri.md)

---

## Genel Mobil Frontend Prensipleri

### 1. Tasarım Sistemi

* **Renk Paleti:** Tutarlı renk kullanımı (primary, secondary, error, success)
* **Tipografi:** Okunabilir font boyutları ve ağırlıkları
* **Spacing:** Tutarlı padding ve margin değerleri (8dp/8pt grid sistemi)
* **Iconography:** Standart icon seti kullanımı

### 2. Responsive Tasarım

* Farklı ekran boyutlarına uyum (phone, tablet)
* Landscape ve portrait mod desteği
* Safe area desteği

### 3. Kullanıcı Deneyimi (UX)

* **Loading States:** Skeleton screens, progress indicators
* **Error Handling:** Kullanıcı dostu hata mesajları
* **Empty States:** Boş durumlar için bilgilendirici mesajlar
* **Feedback:** Kullanıcı aksiyonlarına anında geri bildirim

### 4. Erişilebilirlik (Accessibility)

* Content descriptions ve labels
* Touch target boyutları (min 44x44)
* Screen reader desteği
* Yüksek kontrast modu
* Font scaling desteği

### 5. Performans

* Lazy loading
* Image optimization ve caching
* Smooth animations
* Memory management

### 6. Navigasyon

* Bottom navigation, drawer veya tab navigation
* Deep linking desteği
* Back button handling
* Navigation state yönetimi

### 7. Form Yönetimi

* Real-time validation
* Error mesajlarının alan altında gösterilmesi
* Keyboard handling
* Form state persistence (opsiyonel)

### 8. Platform Özellikleri

* Android Material Design 3 uyumu
* iOS Human Interface Guidelines uyumu
* Platforma özgü native his veren arayüz
