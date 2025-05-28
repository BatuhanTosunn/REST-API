
# OpenAPI Tasarımı Ödevi Teslim Raporu

## 👤 Öğrenci Bilgileri
- **Ad Soyad**: Batuhan Emre Tosun
- **Öğrenci Numarası**: 170422019

---

## 📂 OpenAPI YAML Dosyası

- **openapi.yaml** dosyası projeye eklenmiştir.
- Swagger Editor üzerinden test edilmiştir.

### 🔗 GitHub Repo Linki
https://github.com/BatuhanTosunn/REST-API

---

## 📝 API Açıklaması

Bu API, üniversiteye ait çevrim içi kütüphane sistemi için tasarlanmıştır. Üç temel varlık içerir:
- `books`: Kitap bilgileri (CRUD destekler, sayfalama içerir)
- `students`: Öğrenci bilgileri
- `loans`: Ödünç alma işlemleri, iade PATCH ile yapılır

`components/schemas` kısmında her varlık için model tanımlandı. Parametre örneği olarak `BookId`, response örneği olarak `GET /books` için listeleme kullanıldı.

Sayfalama için `GET /books` endpointinde `page` ve `size` query parametreleri tanımlandı. Hata durumları için 400, 404, 500 yanıtları örneklendi.

---

## 🧪 Test Notları (Opsiyonel)

- `GET /books`: Kitap listesi JSON döner
- `POST /books`: Geçerli bir kitap JSON'u ile başarılı 201 döner
- `GET /books/{id}`: Geçersiz UUID için 404 döner

---

## 📌 Ek Açıklamalar

Şema tanımları sadeleştirilerek, test edilebilir ve genişletilebilir yapı kuruldu.
