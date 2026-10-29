# Mevzuat Uyumluluk Tarama Raporu

- **Depo:** `demo2`
- **Dal / commit:** `test-fixture`
- **Model:** `synthetic-fixture`
- **Kapsam:** Sentetik test verisi; yalnızca test akışı
- **Tarih:** 2026-10-29T00:00:00+00:00
- **İncelenen dosya:** 1 / 1
- **Doğrulanmış bulgu:** 5

> Bu rapor otomatik araç tarafından oluşturulmuştur. Bulguları uygulamadan önce kod ve mevzuat kaynağını uzmanla doğrulayın.

## Bulgular

### 1. [HIGH] Desteklenmeyen para birimleri kabul ediliyor

- **Konum:** `payment_rules.py:9`
- **Güven:** 10 / 10
- **Mevzuat kaynağı:** `TEST_FIXTURE_NOT_LAW`, sayfa 1
- **Açıklama:** İşlev izin verilen para birimi listesini kullanmıyor.
- **Öneri:** Para biriminin desteklenenler kümesinde olup olmadığını denetleyin.

**Kod kanıtı:**

> `    return True`

### 2. [MEDIUM] Yeniden deneme sınırı bir fazla kabul ediliyor

- **Konum:** `payment_rules.py:14`
- **Güven:** 9 / 10
- **Mevzuat kaynağı:** `TEST_FIXTURE_NOT_LAW`, sayfa 1
- **Açıklama:** Deneme sayısı sınıra eşit olduğunda yeni denemeye izin veriliyor.
- **Öneri:** Yeni deneme için mevcut deneme sayısının sınırdan küçük olmasını şart koşun.

**Kod kanıtı:**

> `    return attempt <= limit`

### 3. [HIGH] İade tutarı işlem tutarını aşabiliyor

- **Konum:** `payment_rules.py:19`
- **Güven:** 10 / 10
- **Mevzuat kaynağı:** `TEST_FIXTURE_NOT_LAW`, sayfa 1
- **Açıklama:** İşlev iade tutarını ilk işlem tutarıyla karşılaştırmıyor.
- **Öneri:** İade tutarının sıfırdan büyük ve ilk işlem tutarından küçük veya eşit olduğunu denetleyin.

**Kod kanıtı:**

> `    return requested_amount > 0`

### 4. [MEDIUM] Başvuru numarası gizlenmiyor

- **Konum:** `payment_rules.py:24`
- **Güven:** 10 / 10
- **Mevzuat kaynağı:** `TEST_FIXTURE_NOT_LAW`, sayfa 1
- **Açıklama:** Gösterim işlevi başvuru numarasını değiştirmeden döndürüyor.
- **Öneri:** Yalnızca son karakterleri gösterip önceki karakterleri maskeleyin.

**Kod kanıtı:**

> `    return reference`

### 5. [LOW] İşlem ücreti hesaplanmıyor

- **Konum:** `payment_rules.py:29`
- **Güven:** 9 / 10
- **Mevzuat kaynağı:** `TEST_FIXTURE_NOT_LAW`, sayfa 1
- **Açıklama:** Ücret oranı hesaplamada kullanılmıyor.
- **Öneri:** Tutarı ücret oranıyla çarparak işlem ücretini hesaplayın.

**Kod kanıtı:**

> `    return amount`

## Dosya sonuçları

- `payment_rules.py` — **Tarandı**

## Sınırlamalar

- Yalnızca test için sentetik veri; gerçek mevzuat tespiti veya hukukî görüş değildir.
