# TK Cyber Security - Siber Güvenlik Uzmanı Website

Modern, responsive ve interaktif siber güvenlik uzmanı kişisel website'i. Siyah tema, neon yeşil vurgular ve siber güvenlik estetiği ile tasarlanmıştır.

## 🛡️ Özellikler

### Tasarım & UI/UX
- **Siber Güvenlik Teması**: Siyah arka plan, neon yeşil vurgular
- **TK Logo**: Özel tasarlanmış logo ve marka kimliği
- **Responsive Tasarım**: Tüm cihazlarda mükemmel görünüm
- **Modern Animasyonlar**: Smooth scroll, hover efektleri, parallax
- **Glitch Efektleri**: Siber güvenlik temasına uygun görsel efektler

### Teknik Özellikler
- **Vanilla JavaScript**: Modern ES6+ özellikleri
- **CSS3 Animasyonlar**: Keyframe animasyonları ve geçişler
- **Intersection Observer**: Performanslı scroll animasyonları
- **Form Validasyonu**: Gerçek zamanlı form kontrolü
- **Keyboard Navigation**: Klavye ile navigasyon desteği

### Sayfalar & Bölümler
1. **Ana Sayfa (Hero)**: Etkileyici giriş bölümü
2. **Hakkımda**: Profesyonel deneyim ve istatistikler
3. **Beceriler**: Kategorize edilmiş yetenekler ve progress bar'lar
4. **Projeler**: Portföy projeleri ve teknoloji etiketleri
5. **Eğitim**: Zaman çizelgesi formatında eğitim geçmişi
6. **İletişim**: İletişim bilgileri ve form

## 🚀 Kurulum

1. Dosyaları bilgisayarınıza indirin
2. `index.html` dosyasını web tarayıcınızda açın
3. Veya yerel bir web sunucusu kullanın:

```bash
# Python ile
python -m http.server 8000

# Node.js ile
npx serve . -p 8000

# PHP ile
php -S localhost:8000
```

## 📁 Dosya Yapısı

```
tkonline.world/
├── index.html          # Ana HTML dosyası
├── styles.css          # CSS stilleri
├── script.js           # JavaScript fonksiyonları
└── README.md           # Proje dokümantasyonu
```

## 🎨 Renk Paleti

- **Ana Renk**: `#00ff41` (Neon Yeşil)
- **İkincil Renk**: `#ff006e` (Pembe)
- **Vurgu Renk**: `#8338ec` (Mor)
- **Arka Plan**: `#0a0a0a` (Koyu Gri)
- **Kart Arka Plan**: `#1a1a1a` (Orta Gri)
- **Metin**: `#ffffff` (Beyaz)

## 🔧 Özelleştirme

### Renkleri Değiştirme
`styles.css` dosyasındaki CSS değişkenlerini düzenleyin:

```css
:root {
    --primary-color: #00ff41;
    --secondary-color: #ff006e;
    --accent-color: #8338ec;
    /* ... diğer renkler */
}
```

### İçerik Güncelleme
- **Kişisel Bilgiler**: `index.html` dosyasında ilgili bölümleri düzenleyin
- **Projeler**: Proje kartlarını kendi projelerinizle değiştirin
- **Beceriler**: Skill bar yüzdelerini güncelleyin
- **İletişim**: İletişim bilgilerini değiştirin

### Animasyon Hızları
`script.js` dosyasında animasyon sürelerini ayarlayabilirsiniz:

```javascript
// Typing effect hızı
typeWriter(heroSubtitle, originalText, 150); // 150ms

// Scroll animasyon hızı
window.scrollTo({
    top: offsetTop,
    behavior: 'smooth' // 'auto' yaparak animasyonu kapatabilirsiniz
});
```

## 📱 Responsive Breakpoints

- **Desktop**: 1200px+
- **Tablet**: 768px - 1199px
- **Mobile**: 320px - 767px

## 🌟 Öne Çıkan Özellikler

### Animasyonlar
- **Glitch Efekti**: TK logosunda siber güvenlik teması
- **Parallax Scroll**: Hero bölümünde derinlik hissi
- **Progress Bar Animasyonları**: Beceri yüzdelerinde smooth animasyon
- **Hover Efektleri**: Tüm interaktif elementlerde
- **Particle Effects**: Arka planda floating elementler

### JavaScript Özellikleri
- **Intersection Observer**: Performanslı scroll animasyonları
- **Form Validation**: Gerçek zamanlı e-posta kontrolü
- **Notification System**: Başarı/hata mesajları
- **Keyboard Navigation**: Ctrl+Arrow tuşları ile navigasyon
- **Mobile Menu**: Hamburger menü animasyonu

### CSS Özellikleri
- **CSS Grid & Flexbox**: Modern layout sistemleri
- **CSS Variables**: Kolay özelleştirme
- **Backdrop Filter**: Blur efektleri
- **Gradient Backgrounds**: Modern görsel efektler
- **Box Shadows**: Derinlik ve glow efektleri

## 🔒 Güvenlik

- **XSS Koruması**: Form input validasyonu
- **CSRF Koruması**: Form güvenliği
- **Content Security Policy**: Güvenli kaynak yönetimi

## 📈 Performans

- **Lazy Loading**: Görünür elementler için animasyon
- **Throttled Events**: Scroll event optimizasyonu
- **Minified Assets**: Küçük dosya boyutları
- **Optimized Images**: WebP format desteği

## 🌐 Tarayıcı Desteği

- **Chrome**: 60+
- **Firefox**: 55+
- **Safari**: 12+
- **Edge**: 79+

## 📞 İletişim

Website'deki iletişim formu şu anda demo modunda çalışmaktadır. Gerçek form işlevselliği için backend entegrasyonu gereklidir.

### Backend Entegrasyonu
Form verilerini işlemek için:

```javascript
// script.js dosyasında form submit handler'ını güncelleyin
contactForm.addEventListener('submit', async (e) => {
    e.preventDefault();
    
    const formData = new FormData(contactForm);
    
    try {
        const response = await fetch('/api/contact', {
            method: 'POST',
            body: formData
        });
        
        if (response.ok) {
            showNotification('Mesajınız başarıyla gönderildi!', 'success');
        } else {
            showNotification('Bir hata oluştu. Lütfen tekrar deneyin.', 'error');
        }
    } catch (error) {
        showNotification('Bağlantı hatası.', 'error');
    }
});
```

## 🎯 Gelecek Güncellemeler

- [ ] Dark/Light tema toggle
- [ ] Çoklu dil desteği
- [ ] Blog bölümü
- [ ] Portfolio galerisi
- [ ] Online CV indirme
- [ ] Sosyal medya entegrasyonu
- [ ] Analytics entegrasyonu

## 📄 Lisans

Bu proje MIT lisansı altında lisanslanmıştır.

## 🤝 Katkıda Bulunma

1. Fork yapın
2. Feature branch oluşturun (`git checkout -b feature/AmazingFeature`)
3. Commit yapın (`git commit -m 'Add some AmazingFeature'`)
4. Push yapın (`git push origin feature/AmazingFeature`)
5. Pull Request oluşturun

---

**TK Cyber Security** - Dijital dünyayı güvenli hale getirmek için çalışıyoruz! 🛡️ 