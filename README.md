# STM32 ADC Tabanlı Akım ve Direnç Ölçüm Uygulaması

Nucleo-F103RB (STM32F103RB) geliştirme kartı kullanılarak geliştirilen, analog veri okuma (ADC) ile dolaylı akım/direnç hesaplama ve eşik gerilimi kontrolü uygulaması.

## Çalışma Mantığı
* **Devre Topolojisi:** Reosta ve 20 kΩ sabit dirençten oluşan seri gerilim bölücü devresi kullanılmıştır.
* **Analog Okuma:** Devreden alınan gerilim değeri `PA0` pini üzerinden ADC ile okunarak akım ve direnç değerleri dolaylı olarak hesaplanır.
* **Eşik Kontrolü:** Okunan gerilim değeri **2.64V** eşik değerini aştığında `PA5` pinine bağlı LED aktif hale getirilir.

## Donanım ve Araçlar
* **Geliştirme Kartı:** STM32 Nucleo-F103RB
* **IDE:** STM32CubeIDE
* **Kütüphane:** STM32 HAL
* **Pin Yapılandırması:**
  * `PA0`: ADC Girişi (Analog gerilim okuma)
  * `PA5`: GPIO Çıkışı (Durum LED'i)

## Proje İçeriği
* `Core/` – `main.c` ve ilgili kaynak/header dosyaları.
* `21_11_2026_ilk_calisma.ioc` – Pin, ADC ve clock ayarlarını içeren yapılandırma dosyası.
