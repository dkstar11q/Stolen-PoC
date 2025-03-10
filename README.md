# CVE-2024-21413-Microsoft-Outlook-Remote-Code-Execution-Vulnerability
Bu betik, Microsoft Outlook'ta keşfedilen ve CVSS değeri 9.8 olan önemli bir güvenlik açığı olan CVE-2024-21413 için bir kavram kanıtı (PoC) sunmaktadır. MonikerLink hatası olarak adlandırılan bu güvenlik açığı, yerel NTLM bilgilerinin potansiyel sızıntısı ve uzaktan kod çalıştırma olasılığı dahil olmak üzere geniş kapsamlı etkilere sahiptir.

🚀 Kullanım

Bu aracı sorumlu bir şekilde kullanın ve hedef sistemin sahibinden yetki aldığınızdan emin olun. Bu komut dosyası, SPF, DKIM ve DMARC kontrollerini atlayarak bir e-posta göndermek için SMTP kimlik doğrulaması gerektirir ve bu da gerçek dünyadaki bir saldırı senaryosunu daha etkili bir şekilde simüle etmeye yardımcı olur.


python CVE-2024-21413.py --server "<SMTP server>" --port <SMTP port> --username "<SMTP username>" --password "<SMTP password>" --sender "<sender email>" --recipient "<recipient email>" --url "<link URL>" --subject "<email subject>"


Parametreler:

--server: SMTP sunucusu ana bilgisayar adı veya IP'si.
--port: Smtp Server Portu.
--username: Kimlik doğrulama için SMTP sunucusu kullanıcı adı.
--password: Kimlik doğrulama için SMTP sunucu parolası.
--sender: Gönderici eposta adresi
--recipient: alıcı eposta adresi .
--url: E-postaya eklenecek kötü amaçlı yol.
--subject: E-posta konusu.


NTLM kimlik bilgilerini içeren Wireshark yakalama (alternatif olarak impacket de çalıştırabilirsiniz)

🧐 Neden SMTP Kimlik Doğrulaması?
SMTP kimlik doğrulaması, gönderilen e-postanın SPF (Gönderen İlkesi Çerçevesi), DKIM (Etki Alanı Anahtarları Tanımlı Posta) ve DMARC (Etki Alanı Tabanlı Mesaj Kimlik Doğrulama, Raporlama ve Uygunluk) gibi yaygın e-posta doğrulama kontrollerini atladığından emin olmak için bu gösteri için çok önemlidir. Bu güvenlik önlemleri, saldırganların sahte bir adresten e-posta gönderdiği e-posta sahteciliğini tespit etmek ve önlemek için tasarlanmıştır. Kimliği doğrulanmış SMTP kullanarak, gösteri sofistike bir saldırganın bu korumaları nasıl atlatabileceğini yakından taklit ederek test ortamını daha gerçekçi hale getirir ve kapsamlı e-posta güvenliği uygulamalarının önemini vurgular.


📆 Değişiklik Günlüğü
[19. şubat 2024] - Added 0-Click NTLM Leak
Confirmed and managed 0-click NTLM Leak (thanks to JT!)
Not yet published
[18. şubat 2024] - Added 1-click RCE
Managed & confirmed Microsoft Outlook Remote Code Execution (RCE)
Not yet published
[16. şubat 2024] - Initial Release
Initial release showcasing the exploit for CVE-2024-21413.
Credits
Checkpoint has done all the amazing research.
Microsoft Security Advisory
📌 Author
Alexander Hagenah

Website
Twitter
LinkedIn
⚠️ Sorumluluk Reddi
Bu araç yalnızca eğitim ve etik test amaçları için tasarlanmıştır. Sistemlerin izinsiz taranması, test edilmesi veya istismar edilmesi yasa dışı ve etik dışıdır. Hedef sistemlere karşı herhangi bir test veya istismar faaliyetinde bulunmak için açık ve yetkili izniniz olduğundan emin olun.

