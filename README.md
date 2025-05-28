# 📚 University Library API – OpenAPI 3.0 Specification

Bu proje, bir üniversiteye ait çevrim içi kütüphane sistemine yönelik RESTful API tanımını içermektedir. API, OpenAPI 3.0.3 standardına uygun olarak hazırlanmıştır ve kitaplar, öğrenciler ve ödünç alma işlemlerini kapsar.

## 🎯 Amaç

Bu çalışmanın amacı, OpenAPI spesifikasyonunu kullanarak gerçek hayattaki bir senaryoya uygun, yapısal ve anlaşılır bir API tanımı oluşturmaktır. Proje kapsamında Swagger Editor üzerinde test edilebilir bir `openapi.yaml` dosyası hazırlanmıştır.

## 🧱 Varlıklar (Entities)

API aşağıdaki 3 ana varlık üzerine kuruludur:

1. **books** → Kitap bilgileri (başlık, yazar, ISBN, stok vb.)
2. **students** → Öğrenci bilgileri (ad, numara, e-posta, aktiflik durumu)
3. **loans** → Ödünç alma ve iade işlemleri (kitap-id, öğrenci-id, ödünç tarihi, iade tarihi, durum)

## 🔄 Tanımlı Endpoint’ler

### `/books`:
- `GET /books`: Tüm kitapları getirir (`page`, `size` parametreleri ile sayfalama desteklenir)
- `GET /books/{id}`: Tek bir kitabı getirir
- `POST /books`: Yeni kitap ekler
- `PUT /books/{id}`: Kitap günceller
- `DELETE /books/{id}`: Kitap siler

### `/students`:
- `GET /students`, `GET /students/{id}`
- `POST /students`, `PUT /students/{id}`, `DELETE /students/{id}`

### `/loans`:
- `GET /loans`, `GET /loans/{id}`
- `POST /loans`: Kitap ödünç alma
- `PATCH /loans/{id}/return`: Kitap iade etme

## ⚙️ Kullanılan Yapılar

- **components/schemas**: Her varlık için detaylı şema tanımı yapılmıştır.
- **parameters**: Hem `path` hem `query` parametreleri kullanılmıştır.
- **responses**: 200, 201, 400, 404, 500 gibi HTTP durum kodlarına uygun yanıt yapıları eklenmiştir.
- **example**: En az bir endpoint için örnek veri kullanılmıştır.
- **description ve tags**: Açıklamalar ve etiketleme ile okunabilirlik artırılmıştır.
- **sayfalama**: `GET /books` endpoint'inde `page` ve `size` parametreleri kullanılmıştır.

## 🔍 Test ve Doğrulama

OpenAPI dosyası, [Swagger Editor](https://editor.swagger.io) üzerinde test edilmiştir. Tüm endpoint'ler için istek ve yanıt örnekleri kontrol edilmiştir.


## 📌 Not

Bu proje sadece tanımsal (specification-based) bir çalışmadır. Gerçek backend veya frontend kodları içermez. Öğrenim amaçlıdır ve değerlendirme kriterlerine birebir uygun şekilde yapılandırılmıştır.

---

Hazırlayan: Batuhan Emre Tosun 
Ders: Açık Kaynak Kodlu Yazılımlar  
Tarih: 28.05.2023
