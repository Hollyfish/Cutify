# Arda Kabay'ın REST API Metotları

**API Test Videosu:** Link buraya eklenecek

## 1. Üye Olma

* **Endpoint:** POST /auth/register

* **Request Body:**

```json
{
  "email": "kullanici@example.com",
  "password": "Guvenli123!",
  "firstName": "Ahmet",
  "lastName": "Yılmaz"
}
```

* **Response:** 201 Created – Kullanıcı başarıyla oluşturulur.

---

## 2. Kullanıcı Bilgilerini Görüntüleme

* **Endpoint:** GET /users/{userId}

* **Path Parameters:**

  * userId (string, required) – Kullanıcı ID bilgisi

* **Authentication:** Bearer Token gereklidir

* **Response:** 200 OK – Kullanıcı bilgileri başarıyla döndürülür.

---

## 3. Kullanıcı Bilgilerini Güncelleme

* **Endpoint:** PUT /users/{userId}

* **Path Parameters:**

  * userId (string, required)

* **Request Body:**

```json
{
  "firstName": "Ahmet",
  "lastName": "Yılmaz",
  "email": "yeniemail@example.com",
  "phone": "+905551234567"
}
```

* **Authentication:** Bearer Token gereklidir

* **Response:** 200 OK – Kullanıcı bilgileri başarıyla güncellenir.

---

## 4. Kullanıcı Silme

* **Endpoint:** DELETE /users/{userId}

* **Path Parameters:**

  * userId (string, required)

* **Authentication:** Bearer Token gereklidir (kendi hesabını silme veya yönetici yetkisi)

* **Response:** 204 No Content – Kullanıcı başarıyla silinir.
