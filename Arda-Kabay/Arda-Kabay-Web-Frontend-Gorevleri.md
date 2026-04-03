# Arda Kabay'ın Web Frontend Görevleri

**Frontend Domain:** https://cutify-frontend.vercel.app

**Front-end Test Videosu:** Link buraya eklenecek

## 1. Üye Olma (Kayıt) Sayfası

* **API Endpoint:** POST /auth/register
* **Görev:** Kullanıcı kayıt işlemi için web sayfası tasarımı ve implementasyonu

### UI Bileşenleri

* Responsive kayıt formu (desktop ve mobile uyumlu)
* Email input (type="email", autocomplete="email")
* Şifre input (type="password", şifre gücü göstergesi)
* Şifre tekrar input
* Ad (firstName) input (autocomplete="given-name")
* Soyad (lastName) input (autocomplete="family-name")
* Kayıt Ol butonu
* Zaten hesabınız var mı? Giriş Yap linki
* Loading spinner
* Form container (card veya centered layout)

### Form Validasyonu

* HTML5 form validation (required, pattern attributes)
* JavaScript real-time validation
* Email format kontrolü
* Şifre minimum 8 karakter, büyük/küçük harf ve rakam
* Şifre eşleşme kontrolü
* Ad ve soyad boş olamaz
* Buton, tüm alanlar geçerli olmadan aktif olmamalıdır
* Client-side ve server-side validation

### Kullanıcı Deneyimi

* Inline validation mesajları
* Başarılı kayıt sonrası yönlendirme
* 409 Conflict hata mesajı: "Bu email zaten kullanılıyor"
* Double-click submission koruması
* Accessible form labels ve ARIA attributes
* Keyboard navigation desteği

### Teknik Detaylar

* Framework (React, Vue, Angular veya Vanilla JS)
* Form library veya native HTML5 form state
* Loading state yönetimi
* Routing
* SEO meta tag optimizasyonu
* WCAG 2.1 erişilebilirlik desteği

---

## 2. Kullanıcı Profil Görüntüleme Sayfası

* **API Endpoint:** GET /users/{userId}
* **Görev:** Kullanıcı profil bilgilerini görüntüleme

### UI Bileşenleri

* Responsive layout (desktop sidebar + mobile stacked)
* Profil fotoğrafı alanı
* Kullanıcı adı ve soyadı (H1 başlık)
* Email bilgisi (icon + copy to clipboard özelliği)
* Telefon numarası
* Hesap oluşturulma tarihi
* Profili Düzenle butonu
* Hesabı Sil butonu
* Refresh veya auto-refresh
* Breadcrumb navigation (opsiyonel)

### Kullanıcı Deneyimi

* Loading skeleton ekran
* Empty state
* Error state ve retry butonu
* Smooth transition animasyonları
* Avatar placeholder
* Responsive grid
* Print-friendly stil

### Teknik Detaylar

* Lazy loading images
* Image optimization (WebP)
* Client-side caching
* State management
* Routing
* Deep linking
* Meta tags (Open Graph, Twitter Cards)

---

## 3. Profil Düzenleme Sayfası

* **API Endpoint:** PUT /users/{userId}
* **Görev:** Profil düzenleme implementasyonu

### UI Bileşenleri

* Responsive form layout
* Profil fotoğrafı drag & drop upload ve preview
* Ad input (mevcut değer ile dolu)
* Soyad input (mevcut değer ile dolu)
* Email input (düzenlenebilir)
* Telefon maskeli input
* Kaydet butonu
* İptal butonu
* Kaydet butonu değişiklik olunca aktif olmalıdır
* Unsaved changes indicator

### Form Validasyonu

* Email format kontrolü
* Telefon format kontrolü
* Real-time validation
* Değişiklik yoksa kaydet disabled
* File upload validation (type ve size)

### Kullanıcı Deneyimi

* Optimistic UI update
* Success toast/snackbar
* Error rollback
* İptal butonu confirmation dialog
* Beforeunload warning
* Image preview
* Upload progress indicator

### Teknik Detaylar

* Form state management (dirty state dahil)
* Image picker entegrasyonu
* Client-side image compression
* Routing
* Unsaved changes protection
* Local draft persistence

---

## 4. Hesap Silme Akışı

* **API Endpoint:** DELETE /users/{userId}
* **Görev:** Hesap silme UI akışı

### UI Bileşenleri

* Hesabı Sil butonu
* Modal dialog
* Şifre doğrulama (opsiyonel)
* Son onay ekranı
* Çift onay mekanizması

### Kullanıcı Deneyimi

* Destructive action uyarıları
* Geri dönüşü olmayan işlem mesajı
* İptal seçeneği
* Loading indicator
* Logout ve login yönlendirme

### Akış Adımları

1. Profil sayfasında Hesabı Sil butonuna tıklama
2. Onay dialog gösterimi
3. Şifre doğrulama (opsiyonel)
4. Detay uyarı ekranı
5. Silme işlemini gerçekleştirme
6. Giriş ekranına yönlendirme

### Teknik Detaylar

* Modal/Dialog component
* Multi-step flow yönetimi
* Error handling
* Session storage ve localStorage temizleme
* Redirect handling
* Browser history management
