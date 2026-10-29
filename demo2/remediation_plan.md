# Düzeltme Planı

- **Depo:** `demo2`
- **Dal / commit:** `test-fixture`
- **Model:** `synthetic-fixture`
- **Seçilen bulgu:** 2

> Bu dosya yalnızca öneri sunar. Kod değişikliği için kullanıcı onayı gerekir.

## 1. [HIGH] Desteklenmeyen para birimleri kabul ediliyor

- **Konum:** `payment_rules.py:9`
- **Güven:** 10 / 10
- **Mevzuat:** `TEST_FIXTURE_NOT_LAW`, sayfa 1
- **Bulgu:** İşlev izin verilen para birimi listesini kullanmıyor.
- **Önerilen düzeltme:** Para biriminin desteklenenler kümesinde olup olmadığını denetleyin.
- **Kod kanıtı:** `    return True`

## 2. [HIGH] İade tutarı işlem tutarını aşabiliyor

- **Konum:** `payment_rules.py:19`
- **Güven:** 10 / 10
- **Mevzuat:** `TEST_FIXTURE_NOT_LAW`, sayfa 1
- **Bulgu:** İşlev iade tutarını ilk işlem tutarıyla karşılaştırmıyor.
- **Önerilen düzeltme:** İade tutarının sıfırdan büyük ve ilk işlem tutarından küçük veya eşit olduğunu denetleyin.
- **Kod kanıtı:** `    return requested_amount > 0`

## Onay

Uygulamadan önce her değişiklik kullanıcıya gösterilmeli ve açık onay alınmalıdır.
Onaylanan değişiklikler ayrı bir dalda uygulanmalı, test edilmeli ve diff raporlanmalıdır.
