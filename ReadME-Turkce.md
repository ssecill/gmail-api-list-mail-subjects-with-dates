# Gmail API Kullanım Kılavuzu

Bu kılavuz, Gmail API kullanarak belirli tarihler arasındaki e-posta konularını Python ile nasıl listeleyeceğinizi gösterir.

## Gereksinimler

1. Python 3.x
2. Gerekli Python kütüphaneleri:
   - google-api-python-client
   - google-auth-httplib2
   - google-auth-oauthlib
3. Google Cloud Console'da bir proje ve OAuth 2.0 istemci kimlik bilgileri (`credentials.json` dosyası).

## Adımlar

### 1. Gerekli Kütüphaneleri Yükleme

Aşağıdaki komutu kullanarak gerekli kütüphaneleri yükleyin:

```sh
pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib pandas openpyxl
```

### 2. Google Cloud Console'da Proje Oluşturma ve Gmail API'yi Etkinleştirme

1. [Google Cloud Console](https://console.cloud.google.com/) adresine gidin ve projenizi seçin veya yeni bir proje oluşturun.
2. Sol menüden "APIs & Services" (API'ler ve Hizmetler) bölümüne gidin ve "Library" (Kütüphane) seçeneğine tıklayın.
3. Arama çubuğuna "Gmail API" yazın ve çıkan sonuçlardan "Gmail API"ye tıklayın.
4. "Enable" (Etkinleştir) düğmesine tıklayın.

### 3. OAuth 2.0 İstemci Kimlik Bilgilerini Oluşturma

1. Sol menüden "APIs & Services" (API'ler ve Hizmetler) bölümüne gidin ve "Credentials" (Kimlik Bilgileri) seçeneğine tıklayın.
2. "Create Credentials" (Kimlik Bilgileri Oluştur) düğmesine tıklayın ve "OAuth client ID" (OAuth istemci kimliği) seçeneğini seçin.
3. "Application type" (Uygulama türü) olarak "Desktop app" (Masaüstü uygulaması) seçin ve bir ad girin.
4. "Create" (Oluştur) düğmesine tıklayın ve istemci kimliği ve gizli anahtarı alın.
5. `credentials.json` dosyasını indirin ve Python betiğinizin bulunduğu dizine koyun.

### 4. Python Kodunu Çalıştırma

Python kodunu çalıştırın:

```sh
python gmail_api.py
```

Kod ilk çalıştırıldığında, tarayıcınızda OAuth 2.0 yetkilendirme sayfası açılacak ve Google hesabınızla oturum açmanız istenecektir. Yetkilendirme tamamlandığında, kod belirtilen tarih aralığındaki e-posta konularını listeleyecektir.

## Notlar

- `credentials.json` dosyasını Google Cloud Console'dan indirdiğiniz istemci kimlik bilgileriyle doldurun.
- İlk çalıştırmada kimlik doğrulama sürecinde bir yetkilendirme penceresi açılacak ve kullanıcıdan yetkilendirme istenecek. Yetki verildikten sonra bir `token.json` dosyası oluşturulacak ve gelecekte tekrar kimlik doğrulama yapmanıza gerek kalmayacaktır.
- Tarih formatı `YYYY/MM/DD` şeklinde olmalıdır. Kodun içinde belirttiğim tarih aralığını kendi ihtiyacınıza göre değiştirebilirsiniz.

Bu kılavuz, Gmail API'yi kullanarak belirli tarihler arasındaki e-posta konularını listelemenizi sağlar. Herhangi bir sorunuz olursa, yardımcı olmaktan memnuniyet duyarım!
