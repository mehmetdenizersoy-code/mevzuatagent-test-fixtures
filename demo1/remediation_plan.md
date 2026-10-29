# Düzeltme Planı

- **Depo:** `demo1`
- **Dal / commit:** `test-fixture`
- **Model:** `synthetic-fixture`
- **Seçilen bulgu:** 2

> Bu dosya yalnızca öneri sunar. Kod değişikliği için kullanıcı onayı gerekir.

## 1. [HIGH] Ödeme başvurusu gizlenmiyor

- **Konum:** `payment_rules.py:6`
- **Güven:** 10 / 10
- **Mevzuat:** `TEST_FIXTURE_NOT_LAW`, sayfa 1
- **Bulgu:** Maskeleme işlevi girdiyi olduğu gibi döndürüyor.
- **Önerilen düzeltme:** Son dört karakteri koruyup önceki karakterleri maskeleyin.
- **Kod kanıtı:** `    return value`

## 2. [MEDIUM] Sıfır tutar geçerli sayılıyor

- **Konum:** `payment_rules.py:11`
- **Güven:** 10 / 10
- **Mevzuat:** `TEST_FIXTURE_NOT_LAW`, sayfa 1
- **Bulgu:** İşlev sıfır tutara da olumlu yanıt veriyor.
- **Önerilen düzeltme:** Pozitif tutar için sıfırdan büyük olma koşulunu kullanın.
- **Kod kanıtı:** `    return amount >= 0`

## Onay

Uygulamadan önce her değişiklik kullanıcıya gösterilmeli ve açık onay alınmalıdır.
Onaylanan değişiklikler ayrı bir dalda uygulanmalı, test edilmeli ve diff raporlanmalıdır.
