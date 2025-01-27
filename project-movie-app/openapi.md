---
description: How to use TMDB API?
---

# TMDB API

## HOW TO USE

1. Sign Up through [https://www.themoviedb.org/login](https://www.themoviedb.org/login)
2. Get your API KEY
3. You can try on Postman
4. Otherwise you can use it in your application directly

{% hint style="info" %}
You must include an **API key** for authentication. It would look like:

[https://api.themoviedb.org/3/movie/popular?<mark style="color:red;">**api\_key**</mark>=YOUR\_API\_KEY](https://api.themoviedb.org/3/movie/popular?api_key=YOUR_API_KEY\&language=en-US\&page=1)
{% endhint %}



## REQUEST FOR LISTS

#### Example 1

TMDB (The Movie Database) API ашиглан алдартай кинонуудын жагсаалтыг авах хүсэлт.

{% code overflow="wrap" %}
```jsx
https://api.themoviedb.org/3/movie/popular?language=en-US&page=1
```
{% endcode %}

URL бүрэлдэхүүн хэсгүүд

1. **Base URl** \
   Энэ бол бүх TMDb API хүсэлтүүдийн үндсэн хаяг.  [https://api.themoviedb.org/3/](https://api.themoviedb.org/3/)  \
   API-ийн  3 дахь хувилбар гэдгийг илэрхийлж байна.
2. **Endpoint** \
   API-аас авах мэдээллийн төрлийг илэрхийлнэ. _movie/popular_ нь алдартай кинонуудын жагсаалтыг авчирна.
3. **Query Parameters**\
   Хүсэлтийг илүү нарийвчлалтай хийхэд ашиглагдана.\
   &#xNAN;_&#x61;. language=en-US_\
   &#x20;Киноны гарчиг, тайлбар зэрэг текстэн өгөгдлийг ямар хэлээр авахыг заана.\
   _b. page=1_ \
   Үр дүнг хэдэн хуудаснаас эхлэн авахыг заана.



```jsx
const options = {
  method: 'GET',
  headers: {
    accept: 'application/json',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiJmMzk2OTBmOTgzMGNlODA0Yjc4OTRhYzFkZWY0ZjdlOSIsIm5iZiI6MTczNDk0OTM3MS43NDIsInN1YiI6IjY3NjkzOWZiYzdmMTcyMDVkMTBiMGIxMiIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.2r2TerxSJdZGmGVSLVDkk6nHT0NPqY4rOcxHtMNt0aE',
  },
};

const response = await fetch(
    `https://api.themoviedb.org/3/movie/${endpoint}?language=en-US&page=1`,
    options
  );
const resJson = await response.json();

```

#### Sample response

```json
{
  "page": 1,
  "results": [
           {
            "adult": false,
            "backdrop_path": "/zfbjgQE1uSd9wiPTX4VzsLi0rGG.jpg",
            "genre_ids": [
                18,
                80
            ],
            "id": 278,
            "original_language": "en",
            "original_title": "The Shawshank Redemption",
            "overview": "Imprisoned in the 1940s for the double murder of his wife and her lover, upstanding banker Andy Dufresne begins a new life at the Shawshank prison, where he puts his accounting skills to work for an amoral warden. During his long stretch in prison, Dufresne comes to be admired by the other inmates -- including an older prisoner named Red -- for his integrity and unquenchable sense of hope.",
            "popularity": 163.526,
            "poster_path": "/9cqNxx0GxF0bflZmeSMuL5tnGzr.jpg",
            "release_date": "1994-09-23",
            "title": "The Shawshank Redemption",
            "video": false,
            "vote_average": 8.708,
            "vote_count": 27349
        },
    ...
  ],
  "total_pages": 500,
  "total_results": 10000
}
```



**results**: Кинонуудын жагсаалт, мэдээлэл

**page**: Хэддэх хуудасны дата вэ

**total\_pages**:Нийт хуудасны тоо.

**total\_results**:  Үр дүнгийн нийт тоо.

Бусад мета өгөгдөл: Хүсэлтийн статус (200, 500 ... ) зэрэг.



## REQUEST FOR IMAGE

1 киноны мэдээллийн хувьд **poster\_path** гэсэн field байгаа. Түүнийг TMDB-ын зурагны endpoint руу хүсэлт явуулна.

```json
 {
            "adult": false,
            "backdrop_path": "/zfbjgQE1uSd9wiPTX4VzsLi0rGG.jpg",
            "genre_ids": [
                18,
                80
            ],
            "id": 278,
            "original_language": "en",
            "original_title": "The Shawshank Redemption",
            "overview": "Imprisoned in the 1940s for the double murder of his wife and her lover, upstanding banker Andy Dufresne begins a new life at the Shawshank prison, where he puts his accounting skills to work for an amoral warden. During his long stretch in prison, Dufresne comes to be admired by the other inmates -- including an older prisoner named Red -- for his integrity and unquenchable sense of hope.",
            "popularity": 163.526,
            "poster_path": "/9cqNxx0GxF0bflZmeSMuL5tnGzr.jpg",
            "release_date": "1994-09-23",
            "title": "The Shawshank Redemption",
            "video": false,
            "vote_average": 8.708,
            "vote_count": 27349
        },
```

#### Example 1

```
https://image.tmdb.org/t/p/w500/9cqNxx0GxF0bflZmeSMuL5tnGzr.jpg
```

URL бүрэлдэхүүн хэсгүүд

1. **Base URl** \
   Энэ нь TMDb-ийн зургийн серверийг илэрхийлнэ [https://image.tmdb.org/t/p/](https://image.tmdb.org/t/p/)\
   Бүх зураг энэхүү үндсэн хаягнаас эхэлж ачаалагдана.
2.  **Size** (**Хэмжээ)** \
    Зургийн өргөнийг 500 пиксел болгон тохируулна.

    w500 нь TMDb-ийн зургийн урьдчилан тодорхойлсон хэмжээний нэг төрөл бөгөөд бусад сонголтуудад w92, w154, w185, w342, w780, original орно.
3. **Path (Зам):**\
   &#xNAN;_<mark style="background-color:yellow;">9cqNxx0GxF0bflZmeSMuL5tnGzr.jpg</mark>_\
   \
   Энэ хэсгийг TMDb API-аас **poster\_path** эсвэл **backdrop\_path** параметрээр өгдөг.



#### **Common Image Sizes on TMDb**

1. **w92**: 92 pixels wide (smallest thumbnail).
2. **w154**: 154 pixels wide.
3. **w185**: 185 pixels wide.
4. **w342**: 342 pixels wide.
5. **w500**: 500 pixels wide.
6. **w780**: 780 pixels wide (large poster size).
7. **original**: Full-resolution image (original size as uploaded).

### Search query

```
https://api.themoviedb.org/3/search/movie?query=game&language=en-US&page=1
```

<mark style="background-color:yellow;">query=END\_HAIH\_UTGA\_BNA</mark>



#### Get all Genre

```
https://api.themoviedb.org/3/genre/movie/list?language=en
```







