# Development 05 — 56 Maddelik Geliştirme Havuzu

Bu havuz, sohbetten **“geliştir”** komutu geldiğinde sıradaki büyük batch'in kaynağıdır. Maddeler uygulanırken mevcut kod korunur; uygulanamayan madde sonraki batch'e taşınır.

## A — Konuşma zekâsı
1. Konu/topic durum modeli ekle.
2. Topic değişimini algılayan güvenli eşik ekle.
3. Son konu TTL davranışı ekle.
4. Kullanıcı başına konuşma bağlamı sınırı ekle.
5. Grup başına bağımsız bağlam anahtarı ekle.
6. Bağlam temizleme yardımcı fonksiyonu ekle.
7. Aynı anlamlı sorularda cevap çeşitlendirmeyi iyileştir.
8. Çok kısa takip mesajlarında güvenli bağlam geri dönüşünü iyileştir.
9. Önceki bot cevabına referans veren takip sorularını destekle.
10. Düşük güven skorunda güvenli fallback davranışını standartlaştır.
11. Cevap tekrarlarını daha güçlü filtrele.
12. Konuşma motoru için kalite metriklerini kalıcılaştır.

## B — Öğrenme ve veri kalitesi
13. Yeni soru-cevap kayıtları için kalite puanı alanı ekle.
14. Boş/çok kısa girişleri import öncesi filtrele.
15. Aynı cümlenin farklı yazımlarını güvenli eşleştirme katmanı ekle.
16. Türkçe karakter normalizasyonunu veri kaybı olmadan standardize et.
17. JSONL/JSON/CSV/TXT import raporu oluştur.
18. Import edilen kayıt sayısını audit tablosuna yaz.
19. Atlanan kayıt nedenlerini sınıflandır.
20. Hatalı kayıtları ayrı raporla.
21. `okunacak` klasöründe kilit/yarım dosya koruması ekle.
22. Import sonrası dosya taşıma işlemini atomik hale getir.
23. GitHub import watcher için tekrar işleme korumasını güçlendir.
24. Veri kalite taraması komutu ekle.

## C — Oyun motoru
25. Oyun başına ayrıntılı oyuncu istatistiği ekle.
26. Oyun başına doğru/yanlış cevap oranı ekle.
27. Ortalama cevap süresi metriği ekle.
28. 30 seviyelik turun özet istatistiklerini kalıcılaştır.
29. Oyun bazlı başarı rozetlerini genişlet.
30. Seri galibiyet hesaplamasını standartlaştır.
31. Günlük oyun istatistiği ekle.
32. Haftalık oyun lider tablosu ekle.
33. Aylık oyun lider tablosu ekle.
34. Duplicate guess kontrolünü kalıcı audit ile birleştir.
35. Stale oyun kurtarma durumunu daha görünür hale getir.
36. Oyun veri bankası sağlık kontrolü ekle.

## D — Grup ve kişiselleştirme
37. Grup özel ayar profili altyapısı ekle.
38. Grup başına oyun açık/kapalı ayarı ekle.
39. Grup başına konuşma tonu tercihi altyapısı ekle.
40. Kullanıcı tercihlerini açıkça sınırlayan şema ekle.
41. Tercih değişikliklerini audit et.
42. Grup istatistiklerinde tarih filtresi ekle.
43. Yönetici ayarlarının yetki kontrolünü merkezileştir.
44. Founder/admin ayrımını tek yardımcı fonksiyonda standardize et.

## E — Yönetim, güvenlik ve dayanıklılık
45. Hata trendleri için günlük sayaç ekle.
46. Kritik hata özetini admin ekranına ekle.
47. Retry/flood kontrol istatistiklerini görünür yap.
48. Runtime exception sınıflandırmasını genişlet.
49. Migration sürüm tablosu ekle.
50. Migration uygulama durumunu audit et.
51. Backup doğrulama yardımcı akışı ekle.
52. Rollback planı için güvenli manifest oluştur.

## F — Performans ve bakım
53. DB sorgu gecikmesi için basit histogram/özet metriği ekle.
54. Büyük conversation cache temizleme politikasını iyileştir.
55. Periyodik bakım sonuçlarını Development Center'a yaz.
56. Batch/development durumunu tek kalıcı manifestte tut ve sonraki “geliştir” çağrısında kaldığı yerden devam et.
