==============================================================
  LFS TRANSLATOR  v1.0.15   -   Live for Speed sohbet çevirmeni
==============================================================

NEDİR?
------
Live for Speed (LFS) sunucularında yabancı oyuncuların yazdığı sohbet
mesajlarını anında kendi dilinize çevirir ve mesajın hemen altında,
yalnızca sizin ekranınızda gösterir. Karşı tarafa yazmak istediğinizde
yazdığınız metni istediğiniz dile çevirir.

Desteklenen diller: Türkçe, English, Português (Brasil), Русский,
Español, Deutsch, Français, Polski, Italiano.


KURULUM
-------
1) Bu ZIP'in içindeki  LFSTranslator-Setup.exe  dosyasını çalıştırın.
   (Windows "bilinmeyen yayıncı" uyarısı gösterirse: "Ek bilgi" ->
   "Yine de çalıştır". Program imzasız olduğu için bu uyarı çıkabilir.)
2) LFS klasörünüzü seçin (içinde LFS.exe olan klasör).
   Program, LFS klasörünün içinde "LFSTranslator" adlı yeni bir klasöre
   kurulur. Yönetici izni gerekmez.
3) İlk açılışta dilinizi seçin ve seçenekleri onaylayın. Bitti.

Kurulumdan sonra yapmanız gereken başka bir şey yok:
 - Program, LFS'in InSim özelliğini 29992 portunda kendisi açtırır
   (LFS klasöründeki  data\script\autoexec.lfs  dosyasına birkaç satır
   ekler; eski halinin yedeğini alır). Başka bir InSim programı
   (ör. CarPlay) zaten bir port kullanıyorsa o portu paylaşır.
 - LFS her açıldığında program kendiliğinden arka planda başlar.
   Pencere açılmaz. Açmak için sağ alttaki simgeye tıklayın veya
   masaüstündeki "LFS Translator" kısayolunu kullanın.


KULLANIM
--------
GELEN MESAJLAR: Hiçbir şey yapmanız gerekmez. Başka dilde bir mesaj
gelince hemen altında çevirisi görünür:   [PT»TR] Herkese merhaba

KARŞI TARAFA YAZMAK: Sohbet kutusuna  /o  + dil harfi + mesajınızı yazın:

    /o e selam nasılsın      ->  İngilizce
    /o b selam nasılsın      ->  Brezilya Portekizcesi
    /o t hello               ->  Türkçe
    /o r  /o s  /o d  /o f  /o p  /o i   ->  Rusça, İspanyolca,
                                              Almanca, Fransızca,
                                              Lehçe, İtalyanca

Bu mesaj sohbete GİTMEZ. Çeviri yalnızca ekranınızda görünür ve panoya
kopyalanır. Sohbeti açıp Ctrl+V ile yapıştırıp gönderirsiniz.
(Ayarlardan "otomatik gönder" seçeneğini açarsanız doğrudan gönderir.)

Diğer komutlar:
    /o lfst            yardım
    /o lfst off        gelen mesaj çevirisini kapat
    /o lfst on         tekrar aç


ÇEVİRİ ALTYAPISI (ÖNEMLİ)
-------------------------
Program çeviri için kendi sunucusu kullanmaz ve API anahtarı/hesap
gerektirmez. Metinleri şu ücretsiz internet servislerine gönderir:
  1) Google Translate (anahtarsız, herkese açık web uç noktaları)
  2) Yedek olarak MyMemory (translated.net)
Yalnızca çevrilecek mesaj metni gönderilir; kullanıcı adı, sunucu bilgisi
gibi başka veri gönderilmez. Mesajlar program tarafından saklanmaz.

Bu servisler ücretsiz ve resmi olmayan uç noktalar olduğu için:
 - Çok yoğun kullanımda geçici olarak hız sınırı koyabilirler. Program
   bu durumda otomatik olarak diğer uç noktaya/yedek servise geçer,
   kalite o sırada biraz düşebilir.
 - Çok kısa mesajlar (3 harften az) ve emojiler çevrilmez.
 - İnternet yoksa çeviri yapılamaz.
 - Servisler ileride değişirse program güncellemesi gerekebilir
   (güncellemeler otomatik gelir).


LFS SÜRÜM UYUMU
---------------
Program LFS 0.8C37 ile test edilmiştir. Bağlanırken önce güncel InSim
biçimini dener; LFS kabul etmezse otomatik olarak eski InSim
biçimlerine geçer. Eski LFS sürümleriyle bu otomatik uyum denenmemiştir.


SORUN GİDERME
-------------
* "LFS açık - InSim bağlantısı bekleniyor" yazıyorsa: LFS'i kapatıp
  yeniden açın. LFS yeniden başlatıldığında (ör. mod indirirken)
  InSim kapanmış olabilir. Oyunda  /insim=29992  yazarak da açabilirsiniz.
* Port değiştirmek isterseniz: program penceresi -> Ayarlar -> InSim portu.
* Başka bir InSim programıyla (ör. CarPlay) aynı anda çalıştırmak için
  ikisi de aynı portu kullanmalı (varsayılan 29992).
* Çeviri gelmiyorsa: program penceresi -> "Günlük dosyasını aç".
  Hata satırlarını bize iletebilirsiniz.
  Günlük konumu: %APPDATA%\LFSTranslator\logs\lfstranslator.log


GÜNCELLEME
----------
Program, yeni sürümü GitHub üzerinden kendiliği kontrol eder ve LFS
kapalıyken sessizce kurar. Ayarlardan kapatılabilir.


KALDIRMA
--------
LFS klasöründeki "LFS Translator Kaldır" kısayoluna çift tıklayın
(veya Windows Ayarlar -> Uygulamalar). Kaldırınca autoexec.lfs'e
eklenen satırlar, otomatik başlatma ve ayarlar silinir.


--------------------------------------------------------------
  ENGLISH (short)
--------------------------------------------------------------
LFS Translator translates Live for Speed chat messages into your language
right below the original message (only on your screen). Run
LFSTranslator-Setup.exe, choose your LFS folder, done. It enables InSim on
port 29992 by itself (edits data\script\autoexec.lfs, backup is kept) and
starts silently in the background whenever LFS starts.

To write to others: type  /o e hello  (e=English, b=Português, t=Türkçe,
r=Русский, s=Español, d=Deutsch, f=Français, p=Polski, i=Italiano).
The message is NOT sent; the translation is shown on your screen and copied
to the clipboard - paste it into chat with Ctrl+V.

Translation uses free, keyless Google Translate web endpoints, with
MyMemory as fallback. Only the message text is sent. Heavy use may hit rate
limits; quality can drop temporarily.

--------------------------------------------------------------
  PORTUGUÊS (resumo)
--------------------------------------------------------------
O LFS Translator traduz as mensagens do chat do Live for Speed para o seu
idioma, logo abaixo da mensagem original (só na sua tela). Execute o
LFSTranslator-Setup.exe, escolha a pasta do LFS e pronto. Ele ativa o
InSim na porta 29992 sozinho (edita data\script\autoexec.lfs, com backup)
e inicia em segundo plano toda vez que o LFS abre.

Para escrever aos outros: digite  /o e hello  (e=English, b=Português,
t=Türkçe, r=Русский, s=Español, d=Deutsch, f=Français, p=Polski,
i=Italiano). A mensagem NÃO é enviada; a tradução aparece na sua tela e é
copiada para a área de transferência - cole no chat com Ctrl+V.

A tradução usa endpoints gratuitos e sem chave do Google Translate, com
MyMemory como reserva. Só o texto da mensagem é enviado. Uso intenso pode
atingir limites; a qualidade pode cair temporariamente.
