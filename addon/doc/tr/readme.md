# Ton Ustası #

* Yazarlar: Hrvoje Katić
* [kararlı sürümü][1] indir
* NVDA uyumluluğu: 2019.3 ve sonrası

Tone Master'a hoş geldiniz! Bu küçük NVDA eklentisini sadece eğlence için ve
aynı zamanda onu kullanırken eğlenmeniz için oluşturdum.

NVDA'nın aşama çubuklarında ve hata bildirimi için kullandığı bip seslerini
duymak yerine NVDA'ya farklı melodiler çaldırmak istemişimdir. Ancak, bu
işlemi yapmak çok kolay değildi. bu yüzden önce süreci kolaylaştırmak
istedim ve Tone Master'ı yazdım. NVDA'nın Mozzart'ı, Beethoven'ın veya
Rolling Stones'un en çok dinlenme almış şarkılarını çaldığını düşünün. Tabii
ki sonuç kulağa eski cep telefonlarındaki zil sesleri gibi gelecek olsa da
yine de komik oluyor.

Ton Ustası, ton veri dosyalarını uygulayarak ton dizilerini çalma sürecini
basitleştirir. Bu dosyalar favori metin düzenleyicinizle düzenlenebilir ve
ardından NVDA ile oynatmak için kaydedilebilir. Talimatlar için okumaya
devam edin!

## Ton veri dosyaları

Tone Master ile ilk müziğinizi çalabilmeniz için önce bir ton veri dosyası
oluşturmanız ve Tone Master'da açmanız gerekir. Basitçe Ton veri dosyaları,
.tdf uzantılı metin dosyalarıdır. Tone Master, ton dizilerini işlemek ve
çalmak için bu dosyaları kullanır. Tone Master'ın Oluşturacağınız müzikleri
başarılı bir şekilde çalabilmesi için ton veri dosyalarının aşağıda
belirtilen talimatlar çerçevesinde oluşturulmaları gerekir.

1. .tdf dosyasındaki her satır *zorunlu* iki nokta üst üste (:) ile ayrılmış
   üç parametre içermelidir. Birinci parametre ton perdesi, ikinci parametre
   ton süresi, üçüncü parametre ise her ton arasındaki sessizlik
   süresidir. Her üç parametrenin de tanımlanması gereklidir. Aksi takdirde
   Tone Master dosyayı çalamaz.
2. Perde ve süre parametreleri tamsayı, sessizlik parametresi ise ondalık
   sayı olarak tanımlanmalıdır.
3. Eğer  .tdf dosyasındaki herhangi bir satırın başında bir diyez işareti
   (#) varsa, Tone Master o satırı bir yorum olarak algılayacak ve
   yoksayacaktır.

Örnek: 3 tonluk bir dizi çalma

1500:100:0.5

1000:100:0.09

500:100:0.7

Bu örnekte, 1. dizideki ilk tonun perdesi 1500, süresi 100 ve 0,5 sessizlik
vardır. İkinci tonun perdesi 1000, süresi 100 ve sessizlik 0,09'dur. ve son
dizideki son ton perdesi 500, süresi 100 ve sessizlik 0,7'dir.

Önemli, Sessizlik parametresinin belirtilmesi zorunludur. Eğer
belirtilmezse, Tone Master Alt Alta bulunan iki dizeyi üst üste algılar ve
beklenmedik sonuçlar alabilirsiniz.

Ton veri dosyalarının yapısına aşina olmak için lütfen eklentiyle birlikte
gelen örnek dosyayı görüntüleyin ve düzenlemeyi deneyin. Örnek dosyayı
"tones" alt klasöründe bulabilirsiniz.

## Kısayol tuşları

* Alt+NVDA+T: Hiçbir hata yoksa, o anda açılmış ton dosyasını çalar.
* Alt+Shift+NVDA+T: Eğer bir ton verisi çalınıyorsa, çalmayı durdurur.
* Alt+NVDA+N: Düzenleme için Not Defteri'nde yeni bir boş ton veri dosyası
  oluşturur ve açar.
* Alt+NVDA+L: Oynatmak için bir ton veri dosyası seçebileceğiniz bir
  iletişim kutusu açar.
* Alt+NVDA+E: Açılmış ton veri dosyasını düzenlemeniz için dosyayı not
  defterinde açar.
* Alt+NVDA+O: Ton veri dosyalarının bulunması gereken "tones" klasörünü
  açar.

## Diğer notlar

Kısayol tuşlarının yanı sıra, Ayrıca NVDA menüsü, Araçlar, Ton Alt Menüsü'ne
giderek ton veri dosyalarını açabilir, oluşturabilir, düzenleyebilir veya bu
dosyaların bulunduğu tones klasörünü açabilirsiniz.

Yeni ton veri dosyası oluşturma iletişim kutusu görüntülendiğinde, dosya
adını .tdf uzantısı olmadan yazın. Dosya uzantısı Tone Master tarafından
otomatik olarak eklenecektir. Herhangi bir ad belirtilmemişse, Tone Master
"untitled.tdf" olan varsayılan dosya adını kullanacaktır. Dosya
oluşturulduğunda Tone Master yeni dosyayı açacak ve düzenlemeniz için Not
Defteri'nde açacaktır. Eğer yeni dosya oluşturmak istemiyorsanız iletişim
kutusundan Escape tuşuna basarak çıkabilrsiniz.

Not: Tone Master, varsayılan olarak Windows ile birlikte geldiğinden ve bu
nedenle herhangi bir bilgisayarda mevcut olması gerektiğinden, ton veri
dosyalarını düzenlemek için Not Defteri'ni kullanır.

Ton veri dosyası açma iletişim kutusu açıkken, açılmak istenen dosyayı
seçmek için ok tuşlarını kullanın ve ardından Enter'a basın. Dosya açmak
istemiyorsanızEscape tuşuna basın.

.tdf dosyaları içeren bir klasör açtığınızda, görüntülemek veya düzenlemek
için bunları metin düzenleyicinizde açabilirsiniz. Ancak, sonuçlarınızı
anında duymak için önce dosyayı Tone Master'da açmanızı tavsiye
ederim. Ardından dosyayı düzenleyebilir, ilerlemenizi kaydedebilir ve her
kaydetmeden sonra dosyanın son halini dinlemek için oynat komutunu
kullanabilirsiniz.

## 1.3 için değişiklikler

* Düzeltildi: Daha yeni NVDA sürümleriyle uyumluluk sorunu düzeltildi.

## 1.2 için değişiklikler

* Düzeltildi: Boş bir ton verisi seçip ardından başka bir ton verisi seçip
  onu çalmaya çalışmanın ton verilerinin çalınmamasıyla sonuçlanması sorunu
  giderildi.

## 1.1 için değişiklikler

* Eklendi: Tonlarca yeni veri dosyası oluşturmak ve düzenlemek için Not
  Defteri'nde açma seçeneği.
* Eklendi: Şu anda yüklü olan ton veri dosyasını Not Defteri'nde düzenleme
  seçeneği.
* İyileştirildi: Hata mesajları artık daha anlaşılabilir.
* İyileştirildi: Tonlar klasörünü açma veya Not Defteri'nde ton verisi
  dosyalarını düzenleme gibi belirli eklenti özelliklerine artık güvenli
  ekranlarda izin verilmemektedir.
* İyileştirildi: Ton verisi oynatımı durdurulursa, kullanıcı NVDA tarafından
  bilgilendirilecektir.
* Düzeltildi: Eğer bir ton verisi çalınıyorsa, artık başka bir dosya
  çalamazsınız.

## 1.0 için değişiklikler

* İlk sürüm.

[[!tag stable]]

[1]: https://addons.nvda-project.org/files/get.php?file=tmast
