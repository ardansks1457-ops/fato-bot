# Geliştirme Kuralları

- Secret/token/password hiçbir kaynak dosyaya yazılmaz.
- Kullanıcının mevcut verisi silinmez; migration gerekiyorsa güvenli yapılır.
- Yeni özellik mevcut handler/menüyle çakışmamalıdır.
- Aynı iş için ikinci bir paralel sistem kurulmaz; mümkünse mevcut altyapı genişletilir.
- Oyunların temel kuralları korunur: 30 seviye, puanlama ve kalıcı skor.
- Konuşma motoru tek cevap otoritesi olmaya devam eder.
- 100k oyun bankaları gereksiz yere RAM'de topluca tutulmaz.
- Büyük veri dosyaları streaming/lazy-load ile işlenir.
- Hatalar tek bir feature'ın çökmesine yol açmamalıdır.
- Otomatik bakım kaynak kodu kendi kendine değiştirmez; yalnızca güvenli veri/oturum temizliği ve sağlık kontrolü yapar.
- Her geliştirme paketinde değişen dosyalar ve amaçları belirtilir.
