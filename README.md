# Konveyorlu-renk-taniyan-robot-kolu

Renk Tabanlı Ürün Ayrıştırma Robotu
Bu proje, konveyör hattı üzerinde taşınan ürünlerin rengine göre sınıflandırılıp ayrıştırılmasını sağlayan, kamera destekli ve Arduino Uno kontrollü otomatik bir robotik sistemdir.

📖 Proje Hakkında
Bu sistem, endüstriyel otomasyon süreçlerine düşük maliyetli ve verimli bir çözüm sunmayı amaçlamaktadır. Konveyör bandı üzerinde ilerleyen ürünler, bir kamera aracılığıyla taranır, görüntü işleme ve derin öğrenme teknikleriyle renkleri tespit edilir ve 5 serbestlik derecesine sahip bir robot kolu tarafından ilgili renk kutularına hassas bir şekilde yerleştirilir.

Proje, açık kaynaklı donanım ve yazılım bileşenleri kullanılarak geliştirilmiştir. Bu sayede hem donanım hem de yazılım açısından yalın, uygulanabilir ve farklı ihtiyaçlara kolaylıkla uyarlanabilir bir yapıya sahiptir.

✨ Temel Özellikler
Otomatik Sınıflandırma: Ürünleri renklerine göre otomatik olarak tanır ve ayrıştırır.

Görüntü İşleme: Kamera ve gelişmiş algoritmalar ile yüksek doğrulukta renk tespiti yapar.

Robotik Kontrol: 5 serbestlik dereceli robot kolu ile ürünleri hassas bir şekilde kavrar ve hedefe taşır.

Sensör Entegrasyonu: Ürünün varlığını algılayan sensör ile konveyör bandının senkronize çalışmasını sağlar.

Düşük Maliyet: Kolay ulaşılabilir ve uygun maliyetli bileşenler kullanılarak tasarlanmıştır.

Modüler Yapı: Farklı endüstriyel ve eğitim amaçlı projelere kolayca adapte edilebilir.

🛠️ Sistem Bileşenleri
Donanım
Kontrol Ünitesi: Arduino Uno R3

Robot Kol: 5 Serbestlik Dereceli (5-Axis) Robot Kolu

Görüntüleme: Bilgisayara bağlı bir web kamera

Taşıma Sistemi: DC Motor Sürücülü Konveyör Bant

Sensör: Ürün algılama için kızılötesi (IR) veya benzeri bir sensör

Servo Motorlar: Robot kolunun eklemleri için

Yazılım
Görüntü İşleme: Python (OpenCV Kütüphanesi) ve Derin Öğrenme Modelleri

Mikrodenetleyici: Arduino IDE (C/C++)

Haberleşme: Seri Port (Python ve Arduino arasında)

🏗️ Sistemin Mimarisi ve Çalışma Prensibi
Sistem, aşağıdaki adımları izleyerek çalışır:

Ürün konveyör bandı üzerine yerleştirilir ve bant çalışmaya başlar.

Ürün, hattın sonundaki sensör tarafından algılandığında konveyör bandı durur.

Kamera, duran ürünün görüntüsünü alır ve bilgisayara aktarır.

Bilgisayardaki Python betiği, görüntü işleme ve derin öğrenme algoritmalarını kullanarak ürünün rengini (örneğin; kırmızı, yeşil, mavi) tespit eder.

Tespit edilen renk bilgisi, seri haberleşme üzerinden Arduino Uno'ya gönderilir.

Arduino, gelen bilgiye göre robot kolunun servo motorlarını kontrol ederek ürünü alması ve doğru renk kutusuna bırakması için gereken hareket dizisini başlatır.

Robot kol ürünü bıraktıktan sonra başlangıç pozisyonuna döner ve konveyör bandı tekrar çalışmaya başlar.

Bağlantı Şeması
Sistemin elektronik bileşenlerinin bağlantı şeması aşağıda Fritzing ile çizilmiştir.
![image](https://github.com/user-attachments/assets/a9e65135-0d82-40f1-82f2-2cab212b57b4)

Arduino Kod Akış Diyagramı
Arduino'ya yüklenen kodun çalışma mantığını gösteren akış diyagramı:
![image](https://github.com/user-attachments/assets/3afaf0b5-28f5-47b9-811b-26fcee13c2e5)

🚀 Kurulum ve Başlatma
Projeyi kendi bilgisayarınızda çalıştırmak için aşağıdaki adımları izleyin:

Depoyu Klonlayın:

Bash

git clone https://github.com/KULLANICI_ADINIZ/PROJE_ADINIZ.git
cd PROJE_ADINIZ
Python Kütüphanelerini Yükleyin:
Gerekli Python kütüphanelerini requirements.txt dosyasından yükleyin.

Bash

pip install -r requirements.txt
(Not: requirements.txt dosyanız yoksa, kullandığınız kütüphaneleri (örn: pip install opencv-python pyserial tensorflow) buraya ekleyebilirsiniz.)

Arduino IDE'yi Kurun:
Arduino'nun resmi web sitesinden IDE'yi indirin ve kurun.

Arduino_Kodu klasöründeki .ino uzantılı dosyayı açın.

Gerekli kütüphaneleri (örneğin Servo.h) Arduino IDE'nin Kütüphane Yöneticisi'nden yükleyin.

Kodu Arduino Uno'nuza yükleyin.

Sistemi Başlatma:

Donanım bağlantılarının şemaya uygun olduğundan emin olun.

Arduino'yu ve kamerayı bilgisayarınıza bağlayın.

Python betiğini (örneğin main.py) çalıştırın.

Bash

python main.py
Projenin farklı açılardan çekilmiş görselleri.

![image](https://github.com/user-attachments/assets/566d30c0-2710-4097-9dc1-6a6fae73db24)
![image](https://github.com/user-attachments/assets/b2432e0e-f32e-4e56-8d7c-c353cb2cbb32)
![image](https://github.com/user-attachments/assets/87bb5fed-da63-4437-9511-229092ffbcba)


🤝 Katkıda Bulunma
Katkılarınız projeyi daha da ileriye taşıyacaktır! Lütfen bir "pull request" açmaktan veya "issue" oluşturmaktan çekinmeyin.

Projeyi "Fork" edin.

Kendi "Branch"inizi oluşturun (git checkout -b ozellik/YeniOzellik).

Değişikliklerinizi "Commit" edin (git commit -m 'Yeni bir özellik eklendi').

"Branch"inizi "Push" edin (git push origin ozellik/YeniOzellik).

Bir "Pull Request" açın.

📜 Lisans
Bu proje, MIT Lisansı altında lisanslanmıştır. Detaylar için LICENSE dosyasına göz atın.

📧 İletişim
Proje Sorumlusu - Mustafa Yenioğlu,Yunus Emre Nas,Mahmood Ali Mahmood - mustafayenioglu3@gmail.com


