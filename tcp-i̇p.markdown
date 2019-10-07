# TCP/IP Protokolü
TCP / IP(İletim Denetimi Protokolü / Internet Protokolü), ağ aygıtlarını internette birbirine bağlamak için kullanılan bir iletişim protokolleri paketidir. TCP / IP, özel bir ağda (bir intranet veya bir extranet) iletişim protokolü olarak da kullanılabilir.
İletim Kontrol Protokolü (TCP) ve İnternet Protokolü (IP), iki ayrı bilgisayar ağı protokolüdür.
 TCP kısmı veri transfrerinde önemli noklataları belirtirken IP kısmı taşıma yolunu bulmayı belirtir.
 İki bilgisayar aynı protokolleri izlediğinde (aynı kural kümesi) birbirlerini anlayabilir ve veri alışverişi yapabilirler.
 TCP/IP, günümüzde en yaygın olarak kullanılan protokol takımıdır ve TCP/IP protokol yığınına (TCP/IP stack) gömülü, İnternette veri aktarımı için kullanılan 2 protokolü temsil ederler; Transmission Control Protocol (TCP) ve Internet Protocol (IP).
 TCP / IP modeli, hem güncel İnternet mimarisini modellemek hem de ağ üzerinden tüm iletim formları tarafından takip edilen bir kuralları uygulamak için kullanılır

OSI, bu model bir telekomünikasyon veya bilgi işlem sisteminin iletişim işlevlerini karakterize etmek ve standartlaştırmak için kullanılır. OSI, Açık Sistemler Bağlantısı'nı (Open Systems Interconnection) temsil etmektedir. Bu orijinal modeldir, 1983'de Temel Referans Modeli adı altında serbest bırakılmıştır.

Daha sonra 1984 yılında ISO 7498 Standardı olarak standartlaştırılmıştır.
Şu anda, X.200 uyarınca numaralandırılmış ITU-T standartlarına tabidir. Burada ITU-T, Uluslararası Telekomünikasyon Birliği, Telekomünikasyon Standardizasyon Sektörü anlamına gelmektedir. Şimdi TCP / IP 5 Katman Modeli için OSI 7 Katman Modeli ile karşılaştırıldığında daha basit bir model. Ve ARPANET adlı ABD Savunma Bakanlığı paket anahtarlama ağı için geliştirildi. Ve bu nedenle, aynı zamanda DoD modeli olarak da adlandırılır. Şimdi, ARPANET planlaması 1968'de başladı ve kullanıldı ve 1990'da görevden alındı. 1982'de tüm askeri bilgisayar ağları için Birleşmiş Milletler Savunma Bakanlığı standardı olarak ilan edildi ve yaygın şekilde kullanıldı. Şu anda IAB tarafından IETF tarafından sağlanmaktadır.
><img class="irc_mi" src="http://bit.kuas.edu.tw/~csshieh/teach/np/tcpip/dod.gif" onload="typeof google==='object'&amp;&amp;google.aft&amp;&amp;google.aft(this)" width="468" height="390" style="margin-top: 50px;" alt="  ">

 >>##### *TCP/IP Layers*
######  Layer 4 : Application Layer
>Uygulamalar  ve bilgisayarlar arasında ile iletişimi  sağlanmaktadır.Bu katmanda veriyi göndermek isteyen uygulama ve kullandığı dosya biçimi bulunarak gönderilen verinin  türüne göre  farklı protokoller çalıştırılır (HTTP,  SMTP, FTP, Telnet, vs.) ve  programlarla Taşıma protokollerinin haberleşmesi sağlanır. Uygulama Katmanı Taşıma Katmanıyla portlar aracılığıyla haberleşir. Taşıma Katmanına gelen paketin içeriğinin türünün anlaşılmasında rol oynar.

######  Layer 3 : Transport Layer
> Bu katman verinin ne şekilde gönderildiğini gösterir. TCP  (Transmission Control Protocol) ve UDP (User Datagram Protocol) protokolleri bu katmanda çalışır. TCP ve UDP iletim esnasında veriye içinde bazı kontrol bilgilerinin bulunduğu bir başlık (header)  ekler. TCP, kayıpsız veri gönderimi sağlayabilmek için kullanılan protokoldür. Gönderilen veriler için özel bir TCP kabul paketi (TCP ACK) gönderilir ve gelmiş olan paketlerin doğruluğu kontrol edilir. Gönderen taraf, kabul gelmediği sürece pakedi tekrar gönderir, böylece gönderim sağlanmış olur. TCP’de veri iletimi için iki bilgisayar arasında Three-Way Handshake (Üç Zamanlı El Sıkışma) bağlantısı kurulur. UDP’de ise gönderilen paketin ulaşıp ulaşmadığı kontrol edilmez. Bağlantı kurulum işlemleri, veri akış kontrolü ve ttekrar iletim işlemleri yapmayarak iletim süresini azaltır ve ağ üzerinde TCP’ye oranda daha az bant genişliği kaplar. TFTP, SNMP,DNS,RİP  gibi protokoller UDP vasıtasıyla çalışır.
######  Layer 2: IP (Internet Protocol) Layer
>İnternet katmanı, kaynak ve hedef bilgisayarlar arasında veri aktarımından sorumludur, hedef veya kaynak IP adresleri veriye eklenerek verinin hangi bilgisayara gönderileceği belirlenir ve gönderilen paket Veri Bloğu (Datagram) halini alır. Datagram maksimum 65,535 bayt boyutunda olabilir, daha fazla boyutlardaki paketleri IP protokolü yeteri kadar "Datagram"a ayırır.
> >Verileri doğru hedefe yönlendirme yaparken birden fazla rota varsa verilerin en kısa yoldan gönderilmesini sağlar. Buna ek olarak, bir verikatarın gönderileceği bir yolun sorunları varsa, veri birimi alternatif bir yolla gönderilir.
Hedefe ulaşmak için bir datagramın aldığı yola rota adı verilir.
Hataları işleme ve parçalara ayırma ve yeniden birleştirme, bunların hepsini takip eden bölümlerde tartışılmaktadır.
Bu katmanda çalışan protokoller:IP,ICMP,IGMP,ARP'dir.
>ICMP, veri iletimi hatalarını gidermek için IP ile çalışır.

##### Layer 1 :  Network Access Layer
 >Ağ Erişimi katmanı, veriyi fiziksel ağ için hazırlamak için gerekli tüm hizmetleri ve işlevleri yönetir.
> Protokol sistemi, verileri belirli bir LAN sistemi üzerinden ve bir hedef bilgisayarın ağ bağdaştırıcısıyla iletmek için ek hizmetler gerektirir. Bu hizmetler, Ağ Erişimi katmanının kapsamıdır.
>Bu katmanda verinin kablo üzerinde alacağı yapıyı tanımlayarak bir ve sıfırların fiziksel olarak görüntülenmesi sağlanır. Ethernet Ağ Arayüzü Katmanında kullanılan ve veri iletiminin fiziksel görünümünü sağlayan en yaygın kablolu yerel ağ teknolojisidir. Ethernet üç alt katmana sahiptir; LLC (Logic Link Control Layer- Mantıksal Bağlantı Kontrolü), MAC (Media Access Control-Ortam Erişim Kontrolü) ve Pyhsical(Fiziksel). LLC alt katmanında, İnternet Katmanı’ndaki frame(çerçeve)’in hangi protokolle geldiğini belirleyerek iletimin  MAC’a geçişini sağlar. MAC alt katmanında, hedef ve kaynak mac adresleri eklenir. LLC ve MAC, veri bloğuna kendi başlıklarını ekleyerek tam "frame" yapısını oluştururlar. Fiziksel alt katman ise bu "frame"i elektrik sinyaline(kablolu ağda) ya da elektromanyetik dalgalara(kablosuz ağda) dönüştürür.
