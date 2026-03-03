# Arda Kabay'ın Mobil Frontend Görevleri

**Mobile Front-end Demo Videosu:** Link buraya eklenecek

## 1. Üye Olma (Kayıt) Ekranı

* **API Endpoint:** POST /auth/register
* **Görev:** Kullanıcı kayıt işlemi için mobil ekran tasarımı ve implementasyonu

### UI Bileşenleri

* Email input alanı (keyboard type: email)
* Şifre input alanı (secure text entry, şifre gücü göstergesi)
* Şifre tekrar input alanı
* Ad (firstName) input alanı
* Soyad (lastName) input alanı
* Kayıt Ol butonu
* Zaten hesabınız var mı? Giriş Yap linki
* Loading indicator

### Form Validasyonu

* Email format kontrolü (real-time)
* Şifre minimum 8 karakter, büyük/küçük harf ve rakam içermeli
* Şifre eşleşme kontrolü
* Ad ve soyad boş olamaz
* Tüm alanlar doldurulmadan buton aktif olmamalıdır

### Kullanıcı Deneyimi

* Form hataları input altında gösterilmelidir
* Başarılı kayıt sonrası giriş ekranına yönlendirme
* Hata durumlarında kullanıcı dostu mesajlar (409 Conflict: email kullanımda)
* Keyboard dismiss özelliği
* ScrollView kullanımı

### Teknik Detaylar

* State management (form state, loading state, error state)
* Navigation sistemi
* Accessibility desteği

## 2. Kullanıcı Profil Görüntüleme Ekranı

* **API Endpoint:** GET /users/{userId}
* **Görev:** Kullanıcı profil bilgilerini görüntüleme ekranı

### UI Bileşenleri

* Profil fotoğrafı alanı
* Kullanıcı adı ve soyadı başlık olarak
* Email bilgisi (ikonlu)
* Telefon numarası (ikonlu)
* Hesap oluşturulma tarihi
* Profili Düzenle butonu
* Hesabı Sil butonu (kırmızı)
* Pull-to-refresh özelliği

### Kullanıcı Deneyimi

* Loading skeleton ekran
* Empty state görünümü
* Error state ve retry butonu
* Smooth scroll animasyonları
* Avatar placeholder

### Teknik Detaylar

* Lazy loading
* Image caching
* State management
* Navigation
* Deep linking

## 3. Profil Düzenleme Ekranı

* **API Endpoint:** PUT /users/{userId}
* **Görev:** Profil düzenleme ekranı

### UI Bileşenleri

* Profil fotoğrafı değiştirme alanı
* Ad (mevcut değerle dolu)
* Soyad (mevcut değerle dolu)
* Email (düzenlenebilir)
* Telefon numarası (input maskeli)
* Kaydet butonu
* İptal butonu

### Form Validasyonu

* Email format kontrolü
* Telefon format kontrolü
* Real-time validation
* Değişiklik yoksa Kaydet butonu disabled

### Kullanıcı Deneyimi

* Optimistic UI update
* Success toast/snackbar
* Error durumunda rollback
* İptal butonunda confirmation dialog
* Keyboard dismiss

### Teknik Detaylar

* Form state management
* Image picker entegrasyonu
* Image compression
* Navigation
* Unsaved changes warning

## 4. Hesap Silme Akışı

* **API Endpoint:** DELETE /users/{userId}
* **Görev:** Hesap silme UI ve akışı

### UI Bileşenleri

* Hesabı Sil butonu
* Onay dialog'u
* Şifre doğrulama ekranı (opsiyonel)
* Son onay ekranı
* Çift onay mekanizması

### Kullanıcı Deneyimi

* Destructive action uyarıları
* Açık uyarı mesajı (Bu işlem geri alınamaz)
* İptal seçeneği
* Loading indicator
* Başarılı silme sonrası logout ve login ekranına yönlendirme

### Akış Adımları

1. Profil ekranında Hesabı Sil butonuna tıklama
2. İlk onay dialog'u gösterme
3. Şifre doğrulama (opsiyonel)
4. Detaylı uyarı ekranı
5. Silme işlemini gerçekleştirme
6. Login ekranına yönlendirme

### Teknik Detaylar

* Dialog/Modal component
* Multi-step flow yönetimi
* Error handling
* Logout ve navigation reset
