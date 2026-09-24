# Fatoş — Geliştir Komutu Batch Protokolü

## Amaç
Kullanıcı sohbet içinde yalnızca **“geliştir”** dediğinde, küçük parçalara bölmek yerine bir sonraki geliştirme batch'i 50–60 maddelik plan üzerinden ele alınır.

## Kesin davranış
- Varsayılan batch boyutu: **56 madde**.
- Önceki batch'ler korunur; aynı iş tekrar yapılmaz.
- Önce `ROADMAP.md`, `TODO.md`, `CHANGELOG.md`, bu dosya ve gerçek kaynak kod incelenir.
- Bir batch içindeki maddeler bağımlılık sırasına göre uygulanır.
- İlgisiz dosyalara dokunulmaz.
- Kaynak kod değişikliğinden sonra `py_compile` ve AST/statik kontroller yapılır.
- Başarısız veya doğrulanamayan maddeler “beklemede” olarak kaydedilir; başarılıymış gibi işaretlenmez.
- Canlı Telegram/aiogram/aiosqlite testi ortamda yoksa bu açıkça belirtilir.
- Her batch sonunda `CHANGELOG.md`, `TODO.md` ve batch durum kaydı güncellenir.

## Önemli sınır
Bu protokol **ChatGPT'nin kullanım, analiz veya hesaplama limitlerini değiştirmez ve bypass etmez**. Bir TXT/KEY dosyası ChatGPT'ye ek yetki veremez. Bu dosya yalnızca geliştirme iş akışını standartlaştırır. Gerçek GitHub/Work erişimi platform izinleriyle sağlanır.

## Batch ilerlemesi
İlerleme `batch_state.json` ile tutulur. Sohbetten “geliştir” komutu geldiğinde mevcut state baz alınır ve sıradaki batch seçilir.

## Sonuç standardı
Her batch sonunda:
1. Yapılan değişiklikler listesi
2. Değişen dosyalar
3. Kontrol sonuçları
4. Bekleyen maddeler
5. Sonraki batch başlangıç noktası
6. Gerekirse güncel ZIP
sunulur.
