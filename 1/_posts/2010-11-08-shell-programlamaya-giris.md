>>> ### Kabuk (Shell) Programlamaya Giriş

Kabuk kullanıcı ile çekirdek arasında bulunan bir yazılım katmanıdır. Görevi 
kullanıcının yapılmasını istediği işlemleri yorumlayıp çekirdek katmanına aktarmaktır.

#### Shell Türleri
* bash
* zsh
* dash
* csh
* tsh

Yukarıdaki shell türleri gibi daha bir çok shell türü bulunmaktadır. En fazla kullanılan shell türü bash'tir.


Sistemimizdeki bash versionunu `echo $BASH_VERSION` komutuyla öğrenebiliriz.

Sistem ilk açıldığında çalışan bash'dir.Ama;
`ls -al` komutunu verdiğimizde bu komut `/bin/dash` te çalışır.Çünkü `/bin/bash` ile `/bin/dash` arasında boyut farkı vardır.

* `du /bin/bash` => 788k
* `du /bin/dash` => 92k 

Bu çalısma prensibi komutların daha hızlı çalışmasına olanak sağlar.

#### Değişkenler

$ komut satırının promptudur.

$var="merhaba" => burada `var` değişkenine "merhaba" dizgisi atanmıştır.

##### NOT: Atamalarda boşluk kullanılmaz

`echo $var` yada `echo "${var}"` diyerek var değişkeninin içeriğini ekrana yazdırabilirsiniz.

birde tamsayı ataması yapalım `x=3` x'e 3 değeri atandı bu değeri bir artırmak istersek `$ x=$(($x+1))` diyoruz.

set ettiğimiz değeri silmek için `$ unset x` dememiz yeterli.
