---
layout: post
title: GNU Gettext ne işe yarar ? .po ve .mo uzantılı dosyalar 
---

GNU Gettext , .mo ve .po uzantılı dosyalar nedir?
Yazılımımızı (uygulamamızı) oluştururken , genişleyip daha çok yayılacak potansiyelde hazırlamalıyız. Yayılmasından kasıt , uygulamayı oluşturduğumuz dilden (genelde bu dil İngilizce olmakta) farklı dilleri destekler nitelikte olmalı. Ayrıca bu özellik yazılımımızn gelişmesine oldukça katkı sağlar.
Peki bu nasıl sağlanır?

Açık kaynak dünyası bize bu konuda GNU Gettext’i sunmuştur. GNU Gettext bir çeviri kütüphanesidir. Biraz daha açmak gerekirse ; GNU Gettext bize dil desteği sağlar ve PHP uygulamalarımızı ulusallaştırmak için kullanacağımız Yerel Dil Desteği arayüzünü gerçekler. Oluşturulan bu arayüz hem kullanıcıya hemde programcıya büyük olanak sağlamaktadır.

 Gettext’te , 
msgid anahtarı ve    msgstr    çevirisi yapılmış metin vardır .

    msgid “hello world”

    msgstr “merhaba dünya”

Gettext anahtarı alıp ,bu anahtarı çevirisi yapılmış metinlerle karşılaştırıp çeviriyi bulup bize sunamktadır.
Gettex’te kullanmak üzere , uygulamayı oluşturduğumuz dilden farklı bir dilde yazılan mesajlar .mo uzantılı dosyalarda tutulurlar. .mo dosyaları .po dosyalarından oluşmaktadır. Şimdi bu dosyaları açıklayalım.

**.mo ve .po dosyaları** 

.mo dosyaları (genelde PHP sistemlerin) dil dosyalarının hazırlanmış halidir. .mo dosyalarını herhangi bir programla (notepad , word , dreamweaver..) açmak mümkün değildir , çünkü .mo dosyaları derlenmiş (binary tabanlı) dosyalardır.

.po dosyaları ise .mo dosyalarının derlenmemeiş halidir.  Herhangi bir düzeltme yapacağımız zaman bunu .po dosyasında yapmalıyız. .po dosyasında gerekli düzenlemeyi yapıp kaydettiğimiz an uzantımız .mo olarak değişir yani .po dosyasını derlemiş oluruz. 

Örneğin :
Elimizde Türkçe tr_TR.po dosyası olsun , farklı bir dile çevirmek için (mesela ingilizce olsun, en_EN) tr_TR.po dosyasını açıp gereklü düzenlemeyi yapıp kaydedince(derleyince) tr_TR.mo diye uzantı değişir. Elimizdeki bu .mo dosyasının adını en_EN.mo diye değiştirip ilgili dizine atmalıyız. Daha sonra dil değerimizi en_EN yaptığımız zaman dili ingilizceye çevirmiş oluruz. Bu işlemi bir derleyicide kod yazmayla ilişkilendirirsek tr_TR.po dosyası derleyicide yazdığımız koddur, kaynaktır. tr_TR.mo ise derleyici tarafından derlemiş olduğumuz koddur yani üründür.

“Bir dil bir insan , iki dil iki insan ':-)'”


