# MevzuatAgent Sentetik Test Deposu

> **YALNIZCA TEST İÇİNDİR.** Bu depodaki örnekler bilerek hatalı hazırlanmış
> sentetik kod ve test bulgularıdır. Gerçek mevzuat tespiti, hukukî görüş veya
> gerçek bir sisteme ilişkin güvenlik değerlendirmesi değildir. Üretimde
> kullanmayın.

Bu depo, MevzuatAgent'ın tarama raporu, bulgu sıralama ve onaylı düzeltme
akışlarını güvenli biçimde denemek için `demo1` ve `demo2` örneklerini içerir.
İki örnekte toplam on sentetik bulgu vardır. Mevzuat alanları
`TEST_FIXTURE_NOT_LAW` olarak işaretlenmiştir.

## Örnekler

- `demo1/`: ödeme kuralları için sentetik test kodu ve tarama çıktıları.
- `demo2/`: ikinci bir ödeme kuralları senaryosu ve tarama çıktıları.

Her demo klasöründe `payment_rules.py`, `scan_result.json`, Markdown/HTML
tarama raporları ve en önemli iki bulgu için bir düzeltme planı bulunur.
Düzeltme planı yalnızca öneridir; kod değiştirme veya PR açma yetkisi vermez.

## Kullanım

Bu depoyu yalnızca izole geliştirme/test ortamında kullanın. Örnek kodun
gerçek mevzuata aykırı olduğu iddia edilmemektedir; bulgular sentetik iş
kuralları üzerinden uygulama akışını test eder.

