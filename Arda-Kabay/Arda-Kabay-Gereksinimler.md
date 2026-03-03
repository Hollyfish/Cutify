# Cutify – Gereksinimler

## 1. Giriş Yap (Login)

API Metodu: POST /auth/login
Açıklama: Kullanıcıların email ve şifre bilgileri ile sisteme giriş yapmasını sağlar. Giriş yapan kullanıcıya kimlik doğrulama token’ı verilir. Sistem güvenliği için doğrulama işlemleri yapılır.

## 2. Üye Olma (Kayıt)

API Metodu: POST /auth/register
Açıklama: Yeni kullanıcıların sisteme kayıt olmasını sağlar. Kullanıcı email ve şifre belirleyerek sisteme hesap oluşturabilir. Kişisel bilgilerin güvenli şekilde saklanması sağlanır.

## 3. Berberleri Listele

API Metodu: GET /barbers
Açıklama: Sistemde kayıtlı tüm berberlerin ve sundukları hizmetlerin listelenmesini sağlar. Kullanıcılar ana sayfada berberleri görüntüleyebilir.

## 4. Berber Detayını Görüntüle

API Metodu: GET /barbers/{barberId}
Açıklama: Seçilen berberin detay bilgilerini ve berberin uygun randevu saatlerini görüntülemeyi sağlar.

## 5. Randevu Oluştur

API Metodu: POST /appointments
Açıklama: Kullanıcıların berber ve hizmet seçerek yeni randevu oluşturmasını sağlar.

## 6. Randevu Güncelle

API Metodu: PUT /appointments/{appointmentId}
Açıklama: Kullanıcıların mevcut randevu bilgilerini (tarih, saat veya hizmet) güncellemesini sağlar.

## 7. Randevu Sil

API Metodu: DELETE /appointments/{appointmentId}
Açıklama: Kullanıcıların oluşturdukları randevuları iptal etmesini sağlar. Silme işlemi geri alınamaz.

## 8. Kullanıcı Profilini Görüntüle

API Metodu: GET /users/{userId}
Açıklama: Kullanıcının profil bilgilerini, email, telefon ve hesap bilgilerini görüntülemesini sağlar. Güvenlik için kimlik doğrulama gereklidir.

## 9. Kullanıcı Profilini Güncelle

API Metodu: PUT /users/{userId}
Açıklama: Kullanıcıların ad, soyad, email ve telefon gibi kişisel bilgilerini güncellemesini sağlar. Kullanıcı yalnızca kendi profil bilgilerini değiştirebilir.

## 10. Berber Hizmetlerini Listele

API Metodu: GET /barbers/{barberId}/services
Açıklama: Seçilen berberin sunduğu hizmetlerin listesini görüntülemeyi sağlar.

## 11. Randevu Durumunu Güncelle (Admin)

API Metodu: PUT /appointments/{appointmentId}/status
Açıklama: Yönetici yetkisine sahip kullanıcıların randevu durumunu (Aktif, Tamamlandı, İptal) güncellemesini sağlar.

## 12. Berber Ekle

API Metodu: POST /barbers
Açıklama: Sisteme yeni berber eklenmesini sağlar.

## 13. Berber Güncelle

API Metodu: PUT /barbers/{barberId}
Açıklama: Mevcut berber bilgilerini güncellemeyi sağlar.

## 14. Berber Sil

API Metodu: DELETE /barbers/{barberId}
Açıklama: Sistemde kayıtlı berberin silinmesini sağlar.
