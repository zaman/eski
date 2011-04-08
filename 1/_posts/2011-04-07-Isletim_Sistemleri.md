---                                                                             
layout: post
title: Isletim Sistemleri                                                      
---
### Thread & Process

ProcessStateDiagram.swf animasyonuna https://github.com/zaman/file adresinden
erişebilirsiniz

process; ikili kodun bellekte çalıştırılabilir hale gelmiş haline denir.

scheduling; zaman tahsili

dispatch; scheduling bittiğinde başka bir processe geç

nice; işletim sistemine oncelikli görev belirleme 

scheduler dispatch; kuyruga geri yolla yenisini al

diske yazma işlemi vakit alan bir işlemdir.

en hızlı register'a yazılır.

thread; çalıştırma birimi

polling devamlı olarak kontrol etmek

interrupt process bittiğinde haber vermesi

process state prosesin o anki hali

her process içinden bir çok thread var.

donanıma erişim işletim sistemi tarafndan sistem çağırıları ile yapılır.

threadlar processe ayrılmıs belleği ortak olarak kullanılır.

threadler bir process içinde birden çok çalışma ortamı oluştururlar.

mutex processleri beklet

semophor bitince haber ver

spinlock wc dolu orada spin et

mutual excusion karşılık dışlama mutex açılmıs hali

preempt önleyici

race condion yarış durumu bir kaynaga iki dosyanın birden yazmaya çalısma
durumudur. burada ilk kaynaga ulaşan proses kilitleme yapar diğer proseslerin
kaynağa ulaşmasını engeller.
ilk proses kritik bölge oluşturur.

flock bir proses çalıştığında diğer proseslerin çalışması engeller.


diğer prosesin işi kısa sürecekse buna busy waiting denir. kilitin kalkmasını
beklersin. spinlock yaparsın çekirdeği yorarsın. :(


diske yazan bir proses var baska bir prosesde diske yazmaya kalktı diske yazmak
uzun sürdüğü için bu proses uyuyanlara alınır. yazma işleminden interupt
geldiğinde uyuyan proses hazırlara gecer.

her proses için input output stderr açılır.

bir prosesin belleğine başka bir proses erişemez. ama thredlerde böyle değil.
threadler birbirlerininin belleğine ulaşbilir. threadleri proseslerden ayıran
budur.

