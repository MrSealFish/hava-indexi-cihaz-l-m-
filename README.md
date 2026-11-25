# Kentsel Trafik ve İnce Partikül Madde: Kavramsal Erken Uyarı Cihazı

Lise düzeyinde bir TÜBİTAK 2204-A Lise Öğrencileri Araştırma Projeleri Yarışması çalışması.

## Proje özeti

Bu projede, yoğun trafik saatlerinde ince partikül madde (PM2.5 ve PM10) değerlerinin sakin saatlere göre anlamlı biçimde yüksek olup olmadığı test edilecektir. Veriler, Çevre, Şehircilik ve İklim Değişikliği Bakanlığı'nın kamuya açık Ulusal Hava Kalitesi İzleme Ağı'ndan (havaizleme.gov.tr) alınacaktır. Bulgulara dayanarak kirlilik belirli bir eşiği aştığında uyarı veren bir cihazın kavramsal tasarımı yapılmaktadır.

- **Araştırma sorusu:** Yoğun trafik saatlerinde PM2.5 ve PM10 değerleri sakin saatlere göre anlamlı biçimde yüksek mi?
- **Hipotez:** Yoğun saatlerde (07:30-09:30 ve 17:30-19:30) değerler, sakin saatlere (01:00-04:00) göre anlamlı biçimde yüksektir.
- **Yöntem:** Tek istasyon, en az üç aylık saatlik veri. Bağımsız örneklem t-testi ve basit doğrusal regresyon. Rüzgâr hızı ve sıcaklık ayrıca değerlendirilir.
- **Cihaz:** Yalnızca kavramsal tasarım. Fiziksel prototip yapılmamıştır.

## Klasör içeriği

| Dosya | Açıklama |
|---|---|
| `proje-sitesi/index.html` | Çift dilli (Türkçe/English) proje tanıtım sitesi. Giriş, yöntem, cihaz, slayt sunumu ve kaynaklar. |
| `proje-sitesi/gorsel.png` | Proje sitesinde kullanılan temsili cadde görseli (yapay zekâ ile üretilmiştir). |
| `proje-sitesi/ic_yapi.png` | Cihazın kavramsal iç yapı çizimi (yapay zekâ ile üretilmiştir). |
| `proje-sitesi/blok_semasi.svg` | Cihazın bileşenlerini ve veri akışını gösteren hareketli kavramsal blok şeması. |
| `el-etkilesim/index.html` | Kamera ile el takibi yapan ayrı etkileşimli uygulama. İşaret parmağıyla parça ve bağlantıların işlevini gösterir. |
| `proje-raporu.pdf` | Taslak proje raporu. Görseller ve bölüm yapısı hazır, sayısal bulgular boş. |
| `rapor_sadelestirilmis_taslak.md` | Sadeleştirilmiş rapor iskeleti (Markdown). |
| `yol_haritasi_hava_kirliligi_trafik.pdf` | Zaman çizelgesi ve adım adım yol haritası. |

## Nasıl açılır

### Proje sitesi

`proje-sitesi/` klasöründe `index.html` dosyasını tarayıcıda açmak yeterlidir. Görseller aynı klasörde olmalıdır.

### El etkileşim uygulaması

Kamera ve el takip modeli nedeniyle sayfayı dosya olarak değil, yerel bir sunucu üzerinden açmak daha güvenilirdir:

```bash
cd el-etkilesim
python3 -m http.server 8000
```

Ardından tarayıcıda `http://localhost:8000/index.html` adresini açın ve "Kamerayı başlat" düğmesine basıp kamera iznini verin.

Gereksinimler ve notlar:
- İlk açılışta el takip modeli internetten yüklenir, bu yüzden internet bağlantısı gerekir.
- Kamera görüntüsü yalnızca tarayıcıda işlenir, hiçbir yere gönderilmez.
- Kamera yoksa ya da izin verilmezse uygulama fare ile de kullanılabilir.

#### Kullanım

- **Parça bilgisi:** İşaret parmağınızı bir parçanın üzerine getirin. Parça vurgulanır, bilgisi yanında ve sağ panelde açılır.
- **Kilitleme:** Başparmak ile işaret parmağını birleştirin. Avucunuzu açınca kilit kalkar.
- **Bağlantı bilgisi:** Parçalar arasındaki çizgilerin yakınına gelin. Çizgi, taşınan veri ya da enerjiyi açıklar.
- **Kamera alanı:** Kamera kutusu ekrana göre boyutlanır. Yakınlaştırma yoktur.

## Açık işler

- [ ] Kullanılacak istasyonun seçilmesi (yıllık %75 yeterlilik, PM2.5 verisinin tam olması)
- [ ] Verinin indirilmesi, temizlenmesi ve analizi
- [ ] WHO ve Türkiye sınır değerlerinin resmi kaynaktan teyit edilmesi
- [ ] Uyarı kademelerinin eşik değerlerinin yazılması
- [ ] Literatür özetinin tam metinlerden yazılması
- [ ] Raporda bulgular, özet ve sonuç bölümlerinin doldurulması
- [ ] Çağrı metninden son başvuru tarihi, alan ve sistem bilgilerinin teyit edilmesi (arama sonuçlarında 4 Ocak 2027, 17.30 görüldü)
- [ ] Kaynakçadaki erişim tarihlerinin eklenmesi
- [ ] El etkileşim uygulamasının farklı tarayıcı ve ışık koşullarında test edilmesi

## Dikkat edilmesi gerekenler

- Yapay zekâ ile üretilen görseller ve metinler "temsili" olarak etiketlenmelidir.
- Cadde görseli Türkiye'den çok Doğu Asya şehirlerine benzediği için sunumda bu durum açıklanmalıdır.
- Önceki taslaklardaki doğrulanmamış sayılar ve kaynaklar (Muş aşım günleri, PM_Bilir doğruluk oranı, Erzurum modeli, 2019 Kara Rapor rakamları) kullanılmamalıdır.
- WHO değerleri 2005 kılavuzuna aittir. 2021 güncellemesi kullanılmalıdır.
- Blok şeması ve el etkileşim uygulaması kavramsal araçlardır. Gerçek bir cihazın davranışını ölçtükleri söylenmemelidir.

## Kaynaklar

- Çevre, Şehircilik ve İklim Değişikliği Bakanlığı, Ulusal Hava Kalitesi İzleme Ağı: https://www.havaizleme.gov.tr
- Hava Kalitesi Bülteni (Nisan 2026): https://webdosya.csb.gov.tr/v2/ced/2026/06/BultenRaporu_2026_Nisan-20260608133454.pdf
- EPA, trafik yoğunluğu ve PM2.5 ilişkisi: https://assessments.epa.gov/risk/document/&deid%3D363222
- Moore, Figliozzi, Bigazzi (2014): https://rd.springer.com/chapter/10.1007%252F978-981-15-0644-4_106
- Greenpeace Akdeniz, 2023 PM10 analizi: https://www.greenpeace.org/static/planet4-turkey-stateless/2024/08/ea70255c-gp_195.pdf
- Dünya Sağlık Örgütü hava kalitesi kılavuzu: https://www.who.int
- TÜBİTAK 2204-A çağrı metni (2025-2026): https://tubitak.gov.tr/sites/default/files/2025-10/2204_A_cagri_metni_2025-2026_08.10.2025.pdf
