# Folder Structure

Багшийнх нь санал болгож буй фолдерийн зохион байгуулалт

```
app/
├── 📂(web) 👈 Zahialagch taliin harah web
│   ├── 📂(components)  👈 Zahialagch taliin harah web geh met componentuud bna
│        ├── FoodCard.ts
│   ├───page.ts
├── 📂 admin
│   ├── layout.tsx 👈  ADMIN LAYOUT WITH SIDEBAR 
│   ├───📂(components)  👈 Categories, Foods geh met componentuud bna 
│        ├─── Categories.tsx ... 
│   ├───📂 menu 
│   ├───📂 order
constants
├───types.ts
```



<mark style="background-color:green;">() хаалт нь URL-ын замд тооцогддоггүй, зөвхөн кодын зохион байгуулалтыг сайжруулахад тусалдаг</mark>

#### Admin web

Зөвхөн админууд хандах эрхтэй байна.&#x20;

*   #### _YOUR\_DOMAIN/**admin/menu**_&#x20;

    Food, Food category нэмэх, хасах, өөрчлөх хэсэг
*   #### _YOUR\_DOMAIN/**admin/menu**_



#### Public үндсэн web&#x20;

Хүссэн хүн бүр орж  менютэй танилцах, хоол захиалах боломжтой байна.&#x20;

```
📂(web)
```

