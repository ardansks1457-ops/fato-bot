# Fatoş Development Center

Bu klasör Fatoş projesinin kalıcı geliştirme protokolüdür.

## Amaç
- Mevcut sistemi koruyarak geliştirmeyi sürdürmek.
- Önceki değişiklikleri kaybetmemek.
- Büyük geliştirme paketlerini izlenebilir hale getirmek.
- Railway üzerinde güvenli ve geri alınabilir değişiklikler yapmak.

## Erişim gerçeği
Bu dosyalar **GitHub veya ChatGPT yetkisi vermez**. Token, parola veya kişisel erişim anahtarı içermez. GitHub erişimi GitHub hesabının/bağlantının gerçek yetkileriyle sağlanır.

## Çalışma biçimi
1. Önce repo ve mevcut kod incelenir.
2. Sadece gerekli dosyalar değiştirilir.
3. Önceki özellikler korunur.
4. Veritabanı değişiklikleri geriye uyumlu yapılır.
5. Python AST/compile kontrolü yapılır.
6. Railway için startup/runtime hataları ayrıca kontrol edilir.
7. Değişiklikler CHANGELOG'a yazılır.
8. Bir sonraki çalışma ROADMAP ve TODO'dan devam eder.
