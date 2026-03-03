# Mobil Backend (REST API Bağlantısı) Görevleri

**REST API Adresi:** https://api.cutify.com/v1

Bu dokümanda mobil uygulamanın REST API ile iletişimini sağlayan backend entegrasyon görevleri listelenmektedir. Mobil uygulama, REST servisleri üzerinden veri alışverişi yapacak şekilde tasarlanmıştır.

---

## Mobil Backend Görevleri

### 1. Üye Olma Servisi

* Endpoint: POST /auth/register
* Görev: Mobil uygulamada kullanıcı kayıt işlemini gerçekleştirme
* İşlevler:

  * Kullanıcı email, password, firstName ve lastName bilgilerini toplama
  * Form validasyonu yapma
  * API'ye POST isteği gönderme
  * Başarılı kayıt sonrası giriş ekranına yönlendirme
  * Hata durumlarını yakalama ve kullanıcıya uygun mesaj gösterme

---

### 2. Kullanıcı Profil Görüntüleme Servisi

* Endpoint: GET /users/{userId}
* Görev: Kullanıcı profil bilgilerini API’den çekme
* İşlevler:

  * JWT token ile kimlik doğrulama
  * Kullanıcı ID ile profil verisini alma
  * Gelen veriyi mobil arayüzde gösterme
  * Token süresi dolduğunda yeniden doğrulama
  * Offline durumda cache’den veri gösterme

---

### 3. Profil Güncelleme Servisi

* Endpoint: PUT /users/{userId}
* Görev: Kullanıcı profil bilgilerini güncelleme
* İşlevler:

  * Profil düzenleme ekranından veri toplama
  * Email ve telefon format doğrulaması
  * API’ye PUT isteği gönderme
  * Başarılı güncelleme sonrası cache güncelleme
  * Optimistic UI update desteği

---

### 4. Hesap Silme Servisi

* Endpoint: DELETE /users/{userId}
* Görev: Kullanıcı hesabını silme
* İşlevler:

  * Silme işlemi için onay dialog’u gösterme
  * API’ye DELETE isteği gönderme
  * Local storage ve cache temizleme
  * Logout ve login ekranına yönlendirme
  * Token geçersiz kılma

---

## Genel Backend Prensipleri

### HTTP Client Yapılandırması

* Base URL: https://api.cutify.com/v1
* Timeout süresi: 30 saniye
* Header bilgileri:

  * Content-Type: application/json
  * Authorization: Bearer token

### Authentication Yönetimi

* JWT token secure storage’da saklanmalıdır
* 401 durumunda token yenileme mekanizması kullanılmalıdır
* Logout işleminde token temizlenmelidir

### Error Handling

* Network hataları yönetilmelidir
* HTTP status kodlarına göre mesaj gösterilmelidir
* Retry mekanizması kullanılmalıdır

### Caching Stratejisi

* GET istekleri cache’lenmelidir
* PUT ve DELETE sonrası cache temizlenmelidir

### Loading States

* Request sırasında loading indicator gösterilmelidir
* Başarılı ve başarısız durumlar kullanıcıya bildirilmelidir

### Logging

* Development ortamında request ve response loglanmalıdır
