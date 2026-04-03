# Arda Kabay'ın REST API Metotları

REST API Adresi: https://cutify-backend.onrender.com/v1

API Test Videosu: Link buraya eklenecek

---

## 1. Üye Olma

- Endpoint: POST /auth/register

- Request Body:
{
  "email": "kullanici@example.com",
  "password": "Guvenli123!",
  "firstName": "Ahmet",
  "lastName": "Yılmaz"
}

- Response: 201 Created – Kullanıcı oluşturulur.

---

## 2. Giriş Yapma

- Endpoint: POST /auth/login

- Request Body:
{
  "email": "kullanici@example.com",
  "password": "Guvenli123!"
}

- Response: 200 OK – Giriş başarılı.

---

## 3. Kullanıcı Bilgilerini Görüntüleme

- Endpoint: GET /users/{userId}

- Response: 200 OK

---

## 4. Kullanıcı Bilgilerini Güncelleme

- Endpoint: PUT /users/{userId}

- Request Body:
{
  "firstName": "Ahmet",
  "lastName": "Yılmaz",
  "email": "yeniemail@example.com",
  "phone": "+905551234567"
}

---

## 5. Kullanıcı Silme

- Endpoint: DELETE /users/{userId}

---

## 6. Berberleri Listeleme

- Endpoint: GET /barbers

---

## 7. Berber Detay Görüntüleme

- Endpoint: GET /barbers/{barberId}

---

## 8. Berber Hizmetlerini Listeleme

- Endpoint: GET /barbers/{barberId}/services

---

## 9. Randevu Oluşturma

- Endpoint: POST /appointments

- Request Body:
{
  "userId": "1",
  "barberId": "1",
  "serviceId": "1",
  "date": "2026-04-05",
  "time": "14:00"
}

---

## 10. Randevu Güncelleme

- Endpoint: PUT /appointments/{appointmentId}

- Request Body:
{
  "date": "2026-04-06",
  "time": "15:00"
}

---

## 11. Randevu Silme

- Endpoint: DELETE /appointments/{appointmentId}

---

## 12. Randevu Durum Güncelleme

- Endpoint: PUT /appointments/{appointmentId}/status

- Request Body:
{
  "status": "Tamamlandı"
}

---

## 13. Berber Ekleme

- Endpoint: POST /barbers

- Request Body:
{
  "name": "Berber Hasan",
  "location": "Isparta",
  "phone": "+905558889977"
}

---

## 14. Berber Güncelleme

- Endpoint: PUT /barbers/{barberId}

---

## 15. Berber Silme

- Endpoint: DELETE /barbers/{barberId}