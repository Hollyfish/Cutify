# Gereksinim Analizi

Tüm gereksinimler çıkarıldıktan sonra proje gereksinimleri tartışılmış ve aşağıdaki gereksinimler belirlenmiştir. Her gereksinim, karşılık geldiği API metodu ve kısa açıklaması ile numaralı olarak listelenmiştir.

---

## Tüm Gereksinimler

1. **Giriş Yapma** – Kullanıcı email ve şifre bilgileri ile sisteme güvenli şekilde giriş yapabilmelidir. (POST /auth/login)

2. **Üye Olma** – Yeni kullanıcılar email ve şifre belirleyerek sisteme kayıt olabilmelidir. (POST /auth/register)

3. **Berberleri Listeleme** – Sistemde kayıtlı tüm berberler ana sayfada listelenebilmelidir. (GET /barbers)

4. **Berber Detay Görüntüleme** – Seçilen berberin detay bilgileri ve boş randevu saatleri gösterilebilmelidir. (GET /barbers/{barberId})

5. **Randevu Oluşturma** – Kullanıcı berber ve hizmet seçerek yeni randevu oluşturabilmelidir. (POST /appointments)

6. **Randevu Güncelleme** – Kullanıcı mevcut randevusunu tarih, saat veya hizmet bilgilerini değiştirerek güncelleyebilmelidir. (PUT /appointments/{appointmentId})

7. **Randevu Silme** – Kullanıcı randevusunu iptal edebilmelidir. (DELETE /appointments/{appointmentId})

8. **Profil Görüntüleme** – Kullanıcı profil bilgilerini görüntüleyebilmelidir. (GET /users/{userId})

9. **Profil Güncelleme** – Kullanıcı ad, soyad, email ve telefon bilgilerini güncelleyebilmelidir. (PUT /users/{userId})

10. **Berber Hizmetlerini Listeleme** – Bir berberin sunduğu hizmetler görüntülenebilmelidir. (GET /barbers/{barberId}/services)

11. **Randevu Durumunu Güncelleme (Admin)** – Yönetici randevu durumunu değiştirebilmelidir. (PUT /appointments/{appointmentId}/status)

12. **Berber Ekleme** – Sisteme yeni berber eklenebilmelidir. (POST /barbers)

13. **Berber Güncelleme** – Mevcut berber bilgileri düzenlenebilmelidir. (PUT /barbers/{barberId})

14. **Berber Silme** – Sistemde kayıtlı berberler silinebilmelidir. (DELETE /barbers/{barberId})

---

## Gereksinim Dağılımları

1. [Arda Kabay'ın Gereksinimleri](Arda-Kabay/Arda-Kabay-Gereksinimler.md)
