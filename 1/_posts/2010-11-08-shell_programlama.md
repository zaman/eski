---
layout: post
title: shell programlamaya giriş
---

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

#### if yapısı

{% highlight ruby %}

 `if true; then echo 'true'; fi`
bu komutun çıktısı `$ true` olur.

*** shell programlamada `true`
 ifadesinin dönüş değeri `0`'dır. Yanlıs durumu ise `0` 'dan farklı bir değer ile dönüş yapar.

#### if - else yapısı

file="foo"

if ls $file 1>/dev/null; then
	echo "olan bir dosya"
else
	echo "olmayan dosya"
fi

{% endhighlight %}

 verilen değeri terminalden almak için `file=$1` atamasını yapmamız yeterli.


` $0 ` => programın ismi

 ` $1,$2,$3,$4,$5,$6,$7,$8,$9  ` => terminalden verdiğimiz veriler

` $* ` tüm parametreler

`$#` terminalden girdiğimiz verilerin adeti (`argc`)


`if [ $# -eq 1 ] `

`then`

> `echo "terminalden veri girmediniz" `

`fi`

-eq => " == "

-lt => " < "

-le => " <= "

-gt => " > "

-ge => " >= "

-ne => " != "

