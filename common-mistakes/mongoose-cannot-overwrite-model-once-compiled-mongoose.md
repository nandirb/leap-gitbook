# \[Mongoose] Cannot overwrite model once compiled Mongoose

Алдаа гарч байгаа шалтгаан нь аль хэдийн нэг схем тодорхойлчихсон байгаа мөртлөө дахин схем тодорхойлж байгаатай холбоотой. Схемийг нэг удаа үүсгэчихэд энэ нь глобал объект болчихно. Дараа нь түүнийг шаардлагатай үед нь дуудахаар зохион байгуулах хэрэгтэй.



```javascript
const FoodModel = models['Foods'] || model('Foods', FOOD_SCHEMA);

export { FoodModel }
```



**FoodModel** нь нэг бол аль хэдийн тодорхойлчихсон байгаа models-оос Food гэдэг нь байна <mark style="color:green;">`models['Foods']`</mark>  эсвэл <mark style="color:green;">`model('Foods', FOOD_SCHEMA)`</mark>  гэх кодоор шинээр модел үүсгэж байна.&#x20;

