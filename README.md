# Avrupa Store — Toptan & Tekli Satış Sitesi

Tek dosyalık (`index.html`) statik site. Sunucu ya da veritabanı gerektirmez; siparişler WhatsApp'a hazır mesaj olarak gider.

## Özellikler
- **Tekli / Toptan modu**: Fiyatlar, minimum adet ve sepet buna göre değişir (seçim tarayıcıda hatırlanır).
- **Toptan beden dağılımı**: Beden başına adet + tek dokunuşla "1 asorti seri ekle".
- **Minimum kontrolü**: Toptanda model başı minimum adet dolmadan sipariş verilemez.
- **WhatsApp sipariş**: Sepet + müşteri bilgisi → bedenlere göre gruplu, hazır sipariş mesajı.
- **Kâr hesaplayıcı**: Toptan alıcının brüt kârını anında gösterir.
- Arama, kategori filtresi, sepet hafızası, mobil alt menü, klavye/ekran okuyucu desteği.

## Düzenleme
`index.html` içindeki `<script>` başında:
- `CONFIG` → telefon/WhatsApp, Instagram, adres, Facebook, minimum toptan adet, ödeme seçenekleri
- `PRODUCTS` → ürün adı, kategori, `retail` (tekli fiyat), `wholesale` (toptan fiyat), görsel
- `FAQ` → sık sorulan sorular

Görseller `assets/` klasöründe (800×1000, 4:5 oran, `.webp`). Yeni ürün fotoğrafını aynı ölçüde ekleyip `img` alanına dosya adını (uzantısız) yaz.

> **Not:** Ürünler, fiyatlar, açıklamalar ve ürün görselleri **örnektir**. Mağazanın gerçek ürün fotoğrafları ve fiyatlarıyla değiştirilmelidir. Görseller Unsplash (ticari kullanıma açık lisans) ve yapay zekâ ile üretilmiş, logosuz temsilî görsellerdir.

## Yayına alma
- **Netlify**: klasörü app.netlify.com/drop sayfasına sürükle-bırak.
- **Vercel**: repoyu içe aktar, framework "Other", build komutu yok.
