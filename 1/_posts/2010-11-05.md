---
layout: post
title: sudo olamama sorunu
---

### sudo : "must be setuid root" hatası

> shell ekranına girdiniz ama süper kullanıcı olmaya çalıştığınızda yukarıdaki hatayı mı aldınız. Heyecan yapmayın çünkü bu sorunun çözümü çok kolay.

**Yapmanız gerekenleri sırayla anlatıyorum**

- önce bilgisayarımızı recovery modunda başlatıyoruz
- aşagı kısımda root seçeneği çıkacak onu seçerek devam ediyoruz
- root olduktan sonra aşağıdaki komutları giriyoruz

>- chown root:root /usr/bin/sudo
>- chmod 4755 /usr/bin/sudo 
>

- daha sonra sistemi reboot ediyoruz

**NOT:** Sistem tekrar açıldıktan sonra sudo komutu /etc/sudoers.d/README dosyasının izinlerinde hata verirse " #chmod 422 /etc/sudoers.d/README" diyoruz.

