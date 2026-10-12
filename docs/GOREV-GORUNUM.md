# Görev: görünüm ve okunabilirlik turu (12 Ekim 2026)

> Oturum kapanır ya da bağlam biterse **yeni oturum bu dosyayı okuyup kaldığı yerden devam eder.**
> Aşağıdaki "İlerleme" listesini güncel tut; her adımdan sonra commit'le ve **yalnızca çalışma dalına** it.

## Kullanıcının isteği (birebir)

> ben dışarı çıkıyorum saatlerce vaktin var siteyi temelleri bozmadan görünüş olarak optimizasyon
> olarak sıfırdan tara ve bir sürüm hazırla yayınlamadan önce ben bakacağım. site tasarımını
> seviyorum ama sandık kısmının görünüş olarak çok fazla gelişmesi gerekiyor boş dataları karşı
> tarafa göstermeyelim olabildiğince saklı dursun boş olanlar. daha okunabilir daha profesyonel
> duran bir site istiyorum genel temayı sabit tutarak bunu yap. yaptığın değişiklikleri bana
> listele en sonunda. bu promptu kaydet token biterse tekrar açılınca da devam et

## Kurallar (bu görev için)

- **YAYINLAMA YOK.** `git push origin HEAD:main` yapılmaz. Yalnızca `claude/elegant-tesla-uaepdv`
  dalına commit + push. Kullanıcı bakıp onaylayınca `main`'e alınacak.
- Genel tema sabit: renkler, yazı tipleri, koyu zemin, soyağacı düzeni korunur. Temel yapı
  (veri dosyaları, global'ler, `file://` ile çalışma, test altyapısı) bozulmaz.
- Veri uydurulmaz; görünüm turu veriye dokunmaz.
- **Boş veri gizlenir:** "—" ile dolu satırlar/sütunlar/kartlar mümkün olduğunca gösterilmez
  (değer yoksa satır hiç çizilmez; tüm sütun boşsa sütun çizilmez).
- Öncelik **Sandık** sayfası; sonra soyağacı, harita, kaynakça için okunabilirlik/profesyonellik.
- Optimizasyon: gereksiz yeniden çizim, ağır DOM, büyük dosya yükleri, mobil görünüm.
- Her adımda: `node --test "araclar/test/*.test.js"` + `node araclar/dogrula.js` + Playwright ekran görüntüsü.
- Sonunda kullanıcıya Türkçe, teknik olmayan bir **değişiklik listesi** verilir.

## İlerleme

- [x] 0. Görev kaydı (bu dosya)
- [x] 1. Mevcut durum taraması (ekran görüntüleri: masaüstü + telefon, dört sayfa)
- [x] 2. Sandık: boş veri gizleme (kartta/pencerede "—", "veri yok", "katılım —", boş satır/sütun yok)
- [~] 3. Sandık: görsel düzen — yıl çizelgesi, hizalı satırlar (hükümet, TBMM CB, ara, ayrıntısız yerel), kartlar yenilendi; ince ayar sürüyor
- [ ] 4. Soyağacı, harita, kaynakça: okunabilirlik düzeltmeleri
- [ ] 5. Optimizasyon (yükleme, çizim, mobil)
- [ ] 6. Son denetim (testler, doğrulama, ekran görüntüleri, file://)
- [ ] 7. Değişiklik listesi kullanıcıya
