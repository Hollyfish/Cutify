# Arda Kabay'ın REST API Metotları

REST API Adresi: https://cutify-backend.onrender.com/v1

API Test Videosu: Link buraya eklenecek

---

## 1. Giriş Yap

- Endpoint: POST /auth/login

- Açıklama: Kullanıcı email ve şifre ile giriş yapar ve sistemden token alır.

- Request Body:
{
  "email": "kullanici@example.com",
  "password": "Guvenli123!"
}

---

## 2. Üye Olma

- Endpoint: POST /auth/register

- Açıklama: Yeni kullanıcı oluşturulur.

- Request Body:
{
  "email": "kullanici@example.com",
  "password": "Guvenli123!",
  "firstName": "Ahmet",
  "lastName": "Yılmaz"
}

---

## 3. Berberleri Listeleme

- Endpoint: GET /barbers

- Açıklama: Tüm berberler listelenir.

---

## 4. Berber Detay Görüntüleme

- Endpoint: GET /barbers/{barberId}

- Açıklama: Seçilen berberin detayları ve uygun saatleri gösterilir.

---

## 5. Randevu Oluşturma

- Endpoint: POST /appointments

- Açıklama: Kullanıcı yeni randevu oluşturur.

- Request Body:
{
  "userId": "1",
  "barberId": "1",
  "serviceId": "1",
  "date": "2026-04-05",
  "time": "14:00"
}

---

## 6. Randevu Güncelleme

- Endpoint: PUT /appointments/{appointmentId}

- Açıklama: Randevu bilgileri güncellenir.

- Request Body:
{
  "date": "2026-04-06",
  "time": "15:00"
}

---

## 7. Randevu Silme

- Endpoint: DELETE /appointments/{appointmentId}

- Açıklama: Randevu iptal edilir.

---

## 8. Profil Görüntüleme

- Endpoint: GET /users/{userId}

- Açıklama: Kullanıcı profil bilgileri görüntülenir.

---

## 9. Profil Güncelleme

- Endpoint: PUT /users/{userId}

- Açıklama: Kullanıcı profil bilgileri güncellenir.

- Request Body:
{
  "firstName": "Arda",
  "lastName": "Kabay",
  "email": "arda@example.com",
  "phone": "+905551234567"
}

---

## 10. Berber Hizmetlerini Listeleme

- Endpoint: GET /barbers/{barberId}/services

- Açıklama: Berberin sunduğu hizmetler listelenir.

---

## 11. Randevu Durum Güncelleme (Admin)

- Endpoint: PUT /appointments/{appointmentId}/status

- Açıklama: Randevu durumu değiştirilir.

- Request Body:
{
  "status": "Tamamlandı"
}

---

## 12. Berber Ekleme

- Endpoint: POST /barbers

- Açıklama: Sisteme yeni berber eklenir.

- Request Body:
{
  "name": "Berber Hasan",
  "location": "Isparta",
  "phone": "+905558889977"
}

---

## 13. Berber Güncelleme

- Endpoint: PUT /barbers/{barberId}

- Açıklama: Berber bilgileri güncellenir.

---

## 14. Berber Silme

- Endpoint: DELETE /barbers/{barberId}

- Açıklama: Berber silinir.