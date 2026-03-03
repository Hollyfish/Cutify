# API Tasarımı - OpenAPI Specification

**OpenAPI Spesifikasyon Dosyası:** [cutify-api.yaml](cutify-api.yaml)

Bu doküman, Cutify randevu yönetim sistemi için OpenAPI 3.0 standardına uygun taslak API tasarımını içermektedir.

## OpenAPI Specification

```yaml
openapi: 3.0.3

info:
  title: Cutify API
  description: |
    Cutify berber randevu yönetim sistemi RESTful API tasarımı.

    ## Özellikler
    - Kullanıcı yönetimi
    - Berber listeleme ve detay görüntüleme
    - Randevu yönetimi
    - JWT tabanlı kimlik doğrulama

  version: 1.0.0

servers:
  - url: https://api.cutify.com/v1
    description: Production Server

  - url: http://localhost:3000/v1
    description: Development Server

tags:
  - name: auth
    description: Kimlik doğrulama işlemleri

  - name: users
    description: Kullanıcı yönetimi işlemleri

  - name: barbers
    description: Berber yönetimi işlemleri

  - name: appointments
    description: Randevu yönetimi işlemleri

paths:

  /auth/register:
    post:
      tags:
        - auth
      summary: Kullanıcı kayıt
      description: Sisteme yeni kullanıcı ekler

      requestBody:
        required: true
        content:
          application/json:
            example:
              email: user@example.com
              password: Password123!
              firstName: Ahmet
              lastName: Yılmaz

      responses:
        '201':
          description: Kullanıcı başarıyla oluşturuldu

  /auth/login:
    post:
      tags:
        - auth
      summary: Kullanıcı giriş
      description: Email ve şifre ile giriş yapar

      requestBody:
        required: true
        content:
          application/json:
            example:
              email: user@example.com
              password: Password123!

      responses:
        '200':
          description: Giriş başarılı

  /users/{userId}:
    get:
      tags:
        - users
      summary: Profil görüntüleme

      parameters:
        - name: userId
          in: path
          required: true
          schema:
            type: string

      responses:
        '200':
          description: Profil bilgisi döndü

    put:
      tags:
        - users
      summary: Profil güncelleme

      parameters:
        - name: userId
          in: path
          required: true
          schema:
            type: string

      requestBody:
        required: true
        content:
          application/json:
            example:
              firstName: Ahmet
              lastName: Yılmaz
              email: user@example.com
              phone: "+905551234567"

      responses:
        '200':
          description: Profil güncellendi

    delete:
      tags:
        - users
      summary: Hesap silme

      parameters:
        - name: userId
          in: path
          required: true
          schema:
            type: string

      responses:
        '204':
          description: Kullanıcı silindi

  /barbers:
    get:
      tags:
        - barbers
      summary: Berber listeleme

      responses:
        '200':
          description: Berber listesi döndü

    post:
      tags:
        - barbers
      summary: Berber ekleme (admin)

      responses:
        '201':
          description: Berber eklendi

  /appointments:
    post:
      tags:
        - appointments
      summary: Randevu oluşturma

      requestBody:
        required: true
        content:
          application/json:
            example:
              barberId: "123"
              serviceId: "456"
              date: "2025-01-01"
              time: "14:00"

      responses:
        '201':
          description: Randevu oluşturuldu
```
