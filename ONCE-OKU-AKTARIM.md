# Eczane Flow — manuel GitHub aktarımı

Kaynak sürümü: fabe27d5a92bd7c43584cf6e7266805b25c0c521
Paket tarihi: 14 Eylül 2026

## İçerik
- eczane-flow/: Git tarafından izlenen kaynak dosyaları, README, docs, testler, şema/migration dosyaları ve statik varlıklar.
- eczane-flow-history.bundle: main dalının tam Git geçmişi. GitHub web arayüzüne dosya olarak yüklemeyin; aşağıdaki clone komutu içindir.
- Bu aktarım kılavuzu.

Canlı D1/R2 verileri, kullanıcı yüklemeleri, sırlar ve bağımlılıklar dahil değildir. Sohbetteki fakat kaynak depoya alınmamış eski ek dosyalar dahil değildir. GitHub'a kod yüklemek canlı hosting/veritabanı taşıması değildir. Kurulum ve açık özellikler için README.md'yi okuyun.

## Önerilen ilk aktarım: geçmişi koruyarak
Bilgisayarınızda Git kurulu olmalı. ZIP'i açın. Paketin açıldığı klasörde terminal açın. Kaynak klasörüyle karışmaması için yeni klasör adı kullanıyoruz:

```sh
git clone eczane-flow-history.bundle eczane-flow-github
cd eczane-flow-github
git remote set-url origin https://github.com/dijitalfabrikaaa-maker/eczane-flow.git
git push -u origin main
```

GitHub oturum açmanızı isterse kendi hesabınızla tamamlayın. Şifre veya erişim anahtarınızı sohbetle paylaşmayın. Hedef depoda zaten commit varsa push reddedilebilir: force kullanmayın; hata metnini paylaşın, mevcut değişiklikleri birleştirelim.

## Yalnız dosyaları elle kopyalamak isterseniz
GitHub Desktop ile mevcut özel deponuzu bilgisayara clone edin. Paketteki eczane-flow klasörünün içeriğini clone edilen klasörün köküne kopyalayın; iç içe ikinci eczane-flow klasörü oluşturmayın. Değişiklikleri inceleyip commit ve push yapın. Bu yöntem eski Git geçmişini taşımaz; geçmiş için yukarıdaki bundle yöntemini kullanın. ZIP veya bundle dosyasını kaynak deposuna yüklemeyin.

## Bundan sonraki geliştirmeler
Şu an ChatGPT'nin özel GitHub deposuna erişimi doğrulanmış değil; otomatik push kurulmuş değil.

Kalıcı düzen: GitHub bağlantısı okuma/yazma erişimiyle çalıştığında, önce depodaki güncel değişiklikler alınır, geliştirme bir dalda yapılır, kontrollerden sonra commit/PR ile aktarılır. Sites yayını ayrı adımdır. Doğrudan push ancak erişim doğrulanırsa mümkündür.

Geçici düzen: Her teslimde yeni sürüm ZIP'i ve önceki sürümden değişiklik listesi verilir. Siz aynı yerel GitHub kopyasında değişiklikleri inceleyip commit/push yaparsınız. Silinen dosyalar ayrıca uygulanmalıdır; yalnız ZIP'i üzerine kopyalamak silmeleri taşımaz. GitHub'da başka biri değişiklik yaptıysa geliştirmeden önce güncel kaynak paylaşılmalıdır. İki ayrı kaynağı kontrolsüz değiştirmeyin.

## Doğrulama
GitHub Code sayfasında README.md, app/, components/, docs/ ve package.json kökte görünmelidir. Bundle yöntemiyle ilk yüklemede son commit fabe27d ile başlamalıdır. Geçmiş yedeği git bundle verify ile doğrulandı. Paket bütünlüğü kontrol edildi. Paketleme uygulamanın tüm işlevlerinin veya canlıya hazır olduğunun yeniden test edildiği anlamına gelmez.
