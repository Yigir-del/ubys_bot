# UBYS Bot

Bu proje, UBYS (Üniversite Bilgi Yönetim Sistemi) için oturum açma ve veri çekme işlemlerini gerçekleştiren bir Python botudur.

## Özellikler

- **Giriş Yapma:** Kullanıcı adı ve şifre ile UBYS'ye oturum açma.
- **HTML Veri Çekme:** Sayfa içeriğini alıp analiz etme.
- **Çok Sayfalı Destek:** Birden fazla sayfanın verilerini çekme.
- **Çerez Yönetimi:** Oturum sürekliliğini sağlamak için çerezler kullanır.

## Gereksinimler

Bu projeyi çalıştırmak için aşağıdaki bağımlılıkları yüklemeniz gerekmektedir:

- `requests`
- `beautifulsoup4`

## Kullanım

Aşağıdaki adımları takip ederek botu çalıştırabilirsiniz:

```python
from scraper import Scraper

# Botu başlat
bot = Scraper()

# UBYS giriş bilgileri
credentials = {"username": "kullanici_adi", "password": "sifre"}

# Giriş yap
if bot.post_url("https://ubys.example.com/login", credentials):
    print("Giriş başarılı")
    response = bot.fetch_html("https://ubys.example.com/some-page/")
    print(response)
else:
    print("Giriş başarısız")
```

## Yapılacaklar

- [ ] Hata yönetimini iyileştirme
- [ ] Daha fazla veri çekme özelliği ekleme
- [ ] Test senaryoları oluşturma

## Katkıda Bulunma

Projeye katkıda bulunmak isterseniz pull request açabilir veya bir issue oluşturabilirsiniz.

---

📌 **Not:** Lütfen kullanıcı adı ve şifre gibi bilgileri paylaşmayın ve güvenliğinizi sağlayın.

