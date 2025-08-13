# EmailJS Kurulum Rehberi

Bu rehber, website'inizde EmailJS kullanarak e-posta gönderme sistemini nasıl kuracağınızı açıklar.

## 🚀 Adım 1: EmailJS Hesabı Oluşturma

1. [EmailJS.com](https://www.emailjs.com/) adresine gidin
2. Ücretsiz hesap oluşturun
3. E-posta adresinizi doğrulayın

## 📧 Adım 2: E-posta Servisi Ekleme

1. Dashboard'da "Email Services" sekmesine gidin
2. "Add New Service" butonuna tıklayın
3. Gmail, Outlook veya diğer servislerden birini seçin
4. E-posta hesabınızı bağlayın
5. **Service ID**'yi not alın (örn: `service_abc123`)

## 📝 Adım 3: E-posta Template Oluşturma

1. "Email Templates" sekmesine gidin
2. "Create New Template" butonuna tıklayın
3. Template adını girin (örn: "Contact Form")
4. Aşağıdaki template'i kullanın:

```html
<h2>Yeni İletişim Mesajı</h2>

<p><strong>Gönderen:</strong> {{from_name}}</p>
<p><strong>E-posta:</strong> {{from_email}}</p>
<p><strong>Konu:</strong> {{subject}}</p>

<h3>Mesaj:</h3>
<p>{{message}}</p>

<hr>
<p><em>Bu mesaj TK Cyber Security website'inden gönderilmiştir.</em></p>
```

5. **Template ID**'yi not alın (örn: `template_xyz789`)

## 🔑 Adım 4: Public Key Alma

1. "Account" sekmesine gidin
2. "API Keys" bölümünde **Public Key**'i kopyalayın
3. Bu key'i güvenli bir yerde saklayın

## ⚙️ Adım 5: JavaScript Kodunu Güncelleme

`script.js` dosyasında aşağıdaki değerleri güncelleyin:

```javascript
// EmailJS Configuration
(function() {
    emailjs.init("rGFAYdI-03ZBJqU1u"); // Public key'inizi buraya yapıştırın
})();

// Contact form handling
emailjs.send('tk', 'template_xyz789', templateParams)
    // Service ID ve Template ID'yi buraya yapıştırın
```

### Örnek:
```javascript
emailjs.init("user_abc123def456ghi789");
emailjs.send('tk', 'template_xyz789', templateParams)
```

## 🧪 Adım 6: Test Etme

1. Website'inizi açın
2. İletişim formunu doldurun
3. "Mesaj Gönder" butonuna tıklayın
4. E-posta adresinizi kontrol edin

## 🔧 Sorun Giderme

### E-posta gelmiyor:
- Service ID'yi kontrol edin
- Template ID'yi kontrol edin
- Public Key'i kontrol edin
- Browser console'da hata mesajlarını kontrol edin

### Form çalışmıyor:
- EmailJS CDN linkinin yüklendiğini kontrol edin
- JavaScript kodunda syntax hatası olup olmadığını kontrol edin

## 📊 Ücretsiz Plan Limitleri

- **Aylık 200 e-posta** gönderebilirsiniz
- **2 e-posta servisi** ekleyebilirsiniz
- **5 e-posta template** oluşturabilirsiniz

## 🔒 Güvenlik Notları

- Public Key'inizi paylaşmayın
- Template'lerinizi düzenli olarak kontrol edin
- Spam koruması için rate limiting kullanın

## 📞 Destek

Sorun yaşarsanız:
- EmailJS [dokümantasyonunu](https://www.emailjs.com/docs/) inceleyin
- [EmailJS forumunu](https://www.emailjs.com/community/) ziyaret edin
- [GitHub issues](https://github.com/emailjs/emailjs-com/issues) sayfasını kontrol edin

---

**Not**: Bu rehber EmailJS'in ücretsiz planı için hazırlanmıştır. Daha fazla özellik için premium planları inceleyebilirsiniz. 