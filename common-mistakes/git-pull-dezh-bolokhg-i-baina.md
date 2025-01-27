# \[Git] pull-дэж болохгүй байна

Уг нь доорх 2 дүрмийг баримталж байхад алдаа гарах нөхцөл барагтаа бол үүсэхгүй.

\
1\.  Бичсэн кодоо анги/гэрээсээ гарахасаа өмнө үргэлж push-лэх

```
git add .
git commit -m "Your message"
git push
```

2. Анги/гэртээ очоод **кодондоо өөрчлөлт оруулаагүй байхдаа** pull-дэж авах

```
git pull
```



Гэхдээ заримдаа яалт ч гүй иймэрхүү алдаа гардаг тэ?

<mark style="background-color:yellow;">**Remote repository дээр шинэ commit-үүд нэмэгдчихсэн**</mark> <mark style="background-color:yellow;"></mark><mark style="background-color:yellow;">байгаа бөгөөд,</mark> \
<mark style="background-color:yellow;">**яг одоо нээчихсэн байгаа кодонд чинь тэдгээр commit-ууд байхгүй**</mark> <mark style="background-color:yellow;"></mark><mark style="background-color:yellow;">байна.</mark>&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2025-01-19 at 7.05.10 PM.png" alt=""><figcaption></figcaption></figure>

Одоогийн ажиллаж байгаа компютер дээрх кодондоо өөрчлөлт оруулчихаад push-лэх гэсэн чинь дээрх алдаа гарсан байх. Ингэж засаарай 👇🏻

```
git pull --rebase
```

&#x20;Үүний ардаас `git push`  эсвэл   `git push origin HEAD` эсвэл `git push -u origin master`&#x20;



#### Хэрвээ дээрх арга ажиллахгүй бол үүнийг туршаад үзээрэй

```
git pull origin master --allow-unrelated-histories
```

Үүний ардаас `git push -u origin master`





### Pull-дсэн чинь Conflict үүсвэл яах вэ?&#x20;

Нэг файл доторх Remote дээрх код чиний одоо ажиллаж байгаа компютер дээрхээс зөрөх үед conflict үүсдэг.&#x20;

![](<../.gitbook/assets/Screenshot 2025-01-19 at 7.59.18 PM.png>)\
&#x20;<mark style="color:red;">`CONFLICT`</mark> гэсэн үгийг ард яг аль аль файлууд зөрөөд байгааг нь жагсаалтаар гаргаад өгдөг.&#x20;

Энэ тохиолдолд файл бүр рүү ороод **current** (чиний одоо асаачихсан байгаа ком) эсвэл **incoming** (remote) аль нэгийг нь сонгох юм уу хэрэгтэй хэрэггүйгээ өөрөө нийлүүлж засаад зөв болгох зарчмаар бүгдэнг нь заснаа.&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2025-01-19 at 7.56.09 PM.png" alt=""><figcaption></figcaption></figure>

Зассаныхаа дараа 👇🏻

```
git add .
git rebase --continue 
```

