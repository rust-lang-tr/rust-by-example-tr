# Örneklerle Rust katkı yönergeleri

Örnekle Rust'u (RBE olarak da bilinir) yapmaya gösterdiğiniz ilgi için teşekkür ederiz.
daha iyi! Katkılarınızı almak isteriz. Tüm katkı sahiplerini bekliyoruz
bu bağlantıda veya şu adreste bulabileceğiniz [Rut davranış kurallarına] uyun.
[`CODE_OF_CONDUCT.md`] dosyası bu depoda.

[Rust davranış kuralları]: https://www.rust-lang.org/policies/code-of-conduct
[`CODE_OF_CONDUCT.md`]: [https://github.com/rust-lang/rust-by-example/blob/master/CODE_OF_CONDUCT.md](https://github.com/rust-lang-tr/rust-by-example-tr/blob/master/CODE_OF_CONDUCT.md)

## Lisans

RBE MIT altında çift lisanslıdır ve Apache 2.0 lisanslıdır ve tüm katkılar da öyledir.
Daha fazla ayrıntı için lütfen bu dizindeki [`LICENSE-MIT`] ve [`LICENSE-APACHE`] dosyalarına bakın.

[`LICENSE-MIT`]: [https://github.com/rust-lang/rust-by-example/blob/master/LICENSE-MIT](https://github.com/rust-lang-tr/rust-by-example-tr/blob/master/LICENSE-MIT)
[`LICENSE-APACHE`]: [https://github.com/rust-lang-tr/rust-by-example-tr/blob/master/LICENSE-APACHE](https://github.com/rust-lang-tr/rust-by-example-tr/blob/master/LICENSE-APACHE)

## Çekme İstekleri

RBE'de değişiklik yapmak için lütfen GitHub'da `master` şubesine çekme istekleri gönderin. Bunları inceleyeceğiz ve ya birleştireceğiz ya da değişiklik talep edeceğiz. Travis CI da her şeyi test eder, böylece ondan da geri bildirim alabilirsiniz.

Bir çekme isteğinde eklemeler veya başka değişiklikler yaparsanız, tercihinize göre önceki taahhütleri değiştirmekten veya yalnızca yenilerini eklemekten çekinmeyin. Bağlı olarak birleşmeden önce taahhütlerinizi ezmenizi isteyebiliriz.

## Sorun İzleyici

Sorun izleyiciyi [GitHub'da](https://github.com/rust-lang/rust-by-example/issues) bulabilirsiniz. RBE ile ilgili bir sorun bulduysanız, lütfen orada bir sorun açın.

Aşağıdaki etiketleri kullanıyoruz:

* `enhancement`: Bu, yeni bölümler veya işlevler için herhangi bir istek içindir.
* `bug`: Bu, RBE'de olan ancak yanlış olan veya çalışmayan her şey içindir.
* `discussion`: RBE'de bir şeyi iyileştirme hakkında bir tartışma; bu, yeni geliştirme veya hata sorunlarına yol açabilir.
* `E-mentor`: Bu sorunu, yeni bir katılımcının düzeltmesine yardımcı olmaya adamış biri var!
  Hem geliştirme hem de hata sorunları için geçerli olabilir.

## Geliştirme iş akışı

RBE oluşturmak için [Rust'ı yükleyin] ve ardından:

```bash
$ git clone https://github.com/rust-lang/rust-by-example
$ cd rust-by-example
$ cargo install mdbook
$ mdbook build
```

[Rust'ı yükleyin]: http://rust-lang.org/install.html

Dosyalar en üst düzeydeki 'kitap' dizininde olacaktır; `mdbook serve` içeriği web tarayıcınızda açacaktır.

Testleri çalıştırmak için:

```bash
$ mdbook test
```

Yeni bir bölüm ekliyorsanız, eklemek için `src\SUMMARY.md` dosyasını düzenlemeniz gerekir. Mevcut bir örnek üzerinde ince ayar yapıyorsanız, ilgili dosyayı düzenlemeniz gerekir; bölümlerin dosyalara nereye gittiğinin bir eşlemesini görmek için `src\SUMMARY.md`yi kontrol edin.
