# Strength of Materials — Mukavemet

İngilizce, LaTeX, kısa F → D → S çözümleri için ayrı kaynak deposu.

## Kullanım

Güncel prompt **7996 karakterdir** (UTF-16); 10.000 karakter sınırının altındadır.

[calculator_prompt.txt — raw](https://raw.githubusercontent.com/bugra053/strength-of-materials/main/calculator_prompt.txt) dosyasını açıp **metnin tamamını** ayrı bir Custom Prompt alanına yapıştır. Başlık: `Strength of Materials`. Online tarama/URL okuma aracı gerekir. `online_prompt.txt` aynı içeriğin eş kopyasıdır; iki promptu birlikte yapıştırma.

PDF'lerin platforma yüklenmiş olduğu varsayılmaz. Prompt önce [course_reference.txt](https://raw.githubusercontent.com/bugra053/strength-of-materials/main/course_reference.txt) dosyasını, sonra yalnızca ilgili orijinal sayfa görsellerini okur. Bir bağlantıyı promptta görmek, içeriğinin modele ulaştığını kanıtlamaz. Bu repo modelin veya 7-Cal'in araç erişimini otomatik yapılandırmaz.

## Kaynaklar

- `sources/SOM_Tuto.pdf`: verilen 14 sayfalık dosyanın birebir kopyası.
- `sources/1 (8).pdf`: verilen 10 sayfalık dosyanın birebir kopyası.
- `data/source_manifest.json`: özgün dosya adları, SHA256, sayfa sayıları ve raw bağlantıları.
- `data/page_index.json`: görsel incelemeyle hazırlanan 24 sayfalık konu indeksi.
- `notes/tutorial/pages/` ve `notes/additional/pages/`: orijinal sayfa görüntüleri.
- `notes/*/ocr/`: otomatik ve **doğrulanmamış** OCR. El yazısı, işaretler, üsler, kesirler ve sayılar yanlış çıkabilir. Orijinal görsel/PDF ile kontrol gerekir.
- `course_reference.txt`: incelenen yöntemler, birimler, yalnızca ilgili örneğe ait malzeme değerleri ve doğrudan sayfa bağlantıları. Tam metin transkripsiyonu veya hatasız cevap anahtarı değildir.

Bu iki kaynak ayrı bir tam malzeme/kesit tablosu eki değildir. Notlardaki örnek kuvvetler, boyutlar ve malzeme değerleri değişen sorulara taşınmaz. Standart mekanik denklemler kullanılabilir; eksik sayısal özellik uydurulmaz.

## Çıktı

- F: Yalnızca kullanılacak sembolik formüller.
- D: Gerekli verilenler, geometri, malzeme değerleri, birimler ve kısa işaret yönleri.
- S: Denge/uyumluluk denklemleri, sayısal yerine koyma, gerekli ara işlemler ve birimli kutulu sonuçlar.

Gerekli serbest cisim/kesit çizimleri ve açıkça istenen diyagramlar gösterilir. Bu sürüm çizimler için temel TikZ kullanmayı dener; Kullanıcı kendi 7-Cal görünümünde TikZ çiziminin oluştuğunu bildirdi; bu revizyonda sonradan eklenen özel ok ucu/yerleşim kuralları kaldırılıp ilk sade TikZ yönergesi geri getirildi. Bu oturumda dış görüntüleyicide çizim derlenmedi veya görsel olarak doğrulanmadı. Komutlar düz metin görünürse TikZ yolu o görünümde çalışmıyordur. LaTeX formül desteği tek başına TikZ desteğini kanıtlamaz. F/D/S bölümlerinde denklem ve kısa etiketler kullanılır; kontrol işlemleri ayrıca yazdırılmaz. Uzun açıklama, kaynak paragrafı, gereksiz formül listesi ve atlanan son aritmetik işlem yok. Dış platformun kendi kaynak gösterimlerini prompt tek başına denetleyemez.

## Doğrulama sınırı

Kaynak PDF'lerin birebir kopyalandığı, 24 sayfanın görüntülerinin mevcut olduğu, bağlantı hedefleri ve prompt kapsamı kontrol edildi. Sayfalar görsel olarak incelendi; OCR doğrulanmış transkripsiyon değildir. Kullanıcının dış modeline API isteği gönderilmedi ve tüm ders örneklerinin sayısal olarak doğrulandığı iddia edilmez.
