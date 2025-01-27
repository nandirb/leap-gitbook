# Folder structure

#### () - Групплэх зориулалттай хавтас (Folder Grouping)

() нь групплэх зориулалттай хавтас үүсгэхэд ашиглагддаг бөгөөд энэ нь тухайн хавтас нь URL-д харагдахгүй. Жишээ нь:

```
app/
├── (auth)/
│   ├── login/page.js
│   ├── register/page.js
├── dashboard/page.js
```

(auth) хавтас нь зөвхөн кодыг зохион байгуулахад ашиглагдана, URL-ийн хэсэгт гарч ирэхгүй.

&#x20;login болон register нь URL-д шууд харагдана: _www.your\_domain.com/login_



#### \_ - Тусгай зориулалттай файлууд

\_ тэмдэглэгээ нь Next.js-ийн хуучин хувилбарууд эсвэл тусгай зохион байгуулалтын дүрмүүдтэй холбоотой байдаг. Хэдийгээр Next.js 13-аас хойш шинэ app бүтэцтэй болсон ч зарим тохиолдолд \_ ашиглах боломжтой. Тухайлбал:

* \_app.js: Таны програмын үндсэн тохиргоог хийх (жишээ нь, глобал state, CSS нэмэх).
* \_document.js: Custom HTML бүтэц үүсгэхэд ашиглагддаг.



Дэлгэрэнгүйг доорх холбоосоор орж судлаарай.\
[https://nextjs.org/docs/app/getting-started/project-structure](https://nextjs.org/docs/app/getting-started/project-structure)
