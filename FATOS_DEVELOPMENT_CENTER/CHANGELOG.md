# Runtime güvenlik ve öğrenme hattı düzeltmeleri

- Üretim başlangıcında öğrenme kalite kapısı korunurken GitHub tabanlı remote lock varsayılan olarak kapalı hale getirildi; tek Railway replica için gereksiz heartbeat commit/deploy döngüsü kaldırıldı.
- Çoklu-replica senaryosu için `FATOS_WEB_LEARNING_REMOTE_LOCK_ENABLED=1` ile remote kilit açıkça etkinleştirilebilir.
- Küfür algılamada token sınırı ve noktalı/boşluklu obfuscation kontrolü eklendi; normal kelimelerde yanlış pozitifler azaltıldı.
- Küfür güvenliği final acceptance hattına doğrudan test olarak bağlandı.

# Veri bootstrap ve ölçek düzeltmesi

- Arşivdeki soru-cevap kaynaklarını silmeden ve tamamını RAM'e almadan içe aktaran resumable corpus yolu eklendi.
- Inbox import akışında cümle başına SELECT kaldırıldı; SQLite UNIQUE(normalized) kısıtı ve sınırlı family cache kullanılıyor.
- Boş veritabanında otomatik bootstrap, dolu veritabanında güvenli atlama ve manuel corpus_ingest.py komutu eklendi.
- 50 milyon kayıt hedefinin retrieval veri tabanı olduğu, model eğitimi olmadığı ve kaynak lisansı gerektiği dokümante edildi.

# Changelog

## Development 04
- Development Center eklendi.
- Periyodik DB/oturum retention bakımı eklendi.
- Development sağlık snapshot'ları eklendi.
- Admin paneline Development Center ekranı eklendi.
- Başarım kataloğu genişletildi.
- Başarım ilerleme göstergeleri eklendi.
- 500/1000 oyun puanı başarımları eklendi.
- 100/500 toplam mesaj başarımları eklendi.
- Gelecek geliştirmeler için kalıcı roadmap/rules/checklist sistemi eklendi.

## Development 06 — 56 maddelik Batch Engine
- 56 maddelik ortak geliştirme altyapısı etkinleştirildi.
- Konuşma, veri kalitesi, oyun istatistikleri, grup ayarları, hata trendleri, migration, backup/rollback ve DB latency tabloları eklendi.
- Batch durumu kalıcı manifestte tutuluyor.

- **Development 07:** 56 maddelik işlevsel konuşma, kişiselleştirme, oyun ligi, veri kalite ve operasyon katmanı.

## Development 08 — 56 maddelik güvenilirlik ve ürünleşme batch
- Sağlık, audit, veri taraması, backup checksum, atomic rapor ve batch API katmanı.

## Roadmap reconciliation
- Topic izleme, kontrollü kullanıcı tercihleri, ayrıntılı oyun istatistikleri, haftalık/aylık lig, grup profilleri, hata trendleri, veri kalite taraması, migration sürümleme ve backup/rollback doğrulama mevcut Development 06–08 katmanlarıyla eşleştirildi.
- Aynı iş için ikinci paralel sistem eklenmedi.
- Yayın checklist'i artık özelliklerden ayrı olarak yalnızca son CI/compile/AST/Railway/runtime doğrulamasını takip ediyor.

## CI serialization hardening
- V2 doğrulama workflow'ları ortak `fatos-acceptance-${{ github.ref }}` kuyruğunda sıralandı.
- Final acceptance, final 10x, Turkish coverage, Turkish stress, full learning, dry-run, emoji, caption bridge ve integrity kontrolleri aynı ref üzerinde aynı anda runner/rapor yarışı başlatmayacak şekilde düzenlendi.
- `cancel-in-progress: false` ile başlayan doğrulama çalışması tamamlanmadan sonraki çalışma iptal edilmiyor; hızlı ardışık commitler kuyrukta bekliyor.