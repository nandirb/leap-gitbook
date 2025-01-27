# Хэрхэн оновчтой нэрлэх вэ?

Ерөнхий дүрэм нь их энгийн. **10 жилийн дараа харсан ч шууд ойлгохоор нэр өгөх.**

Гэхдээ хэд хэдэн бичигдээгүй дүрмүүд бий.  Тухайлбал :

## Function

**Функц** нэрлэхдээ **үйл** **үг + нэр үг+ нэмэлт тайлбар** гэж нэрлээрэй.

Жишээ нь: onClickUserCard,  extractDataFromResponse,  isDisabled ...



## Component

**Component** нэрлэхдээ үргэлж **PascalCase**, нэр үг байна.

Жишээ нь:  MovieList , MovieCard, SearchInput, MenuItem

Хэрэв **MovieCard** нэртэй компонент байгаа бол файлаа **MovieCard.tsx** гэж нэрлэх хэрэгтэй.



## Type

**Type** нэрлэхдээ үргэлж **PascalCase**, нэр үг байна.

Жишээ нь:  type **MovieType**, type **MovieCardProps.**

Битгий залхуур л даа. Дараа нь ойлгомжгүй адилхан <mark style="color:red;">type Movie .. component Movie</mark> гэж толгойгоо эргүүлж байхаар зүгээр л аль нь props, аль нь type, аль нь component гэдгийг ялгаад л нэрлэчих л дээ.&#x20;

## Props

Товчлох эсвэл бусад компонентэд өргөн хэрэглэгддэг товчилсон үгсээс аль болох зайлсхий.&#x20;

Жишээ нь: \
`<MovieCard prop={data} />` гэхийн оронд `<MovieCard movie={movieDetails} />`



За одоо сайн болон муу жишээнүүд харуулъя.

<table><thead><tr><th width="177">Сайн </th><th width="176">Муу</th><th>Тайлбар</th></tr></thead><tbody><tr><td>data</td><td>userDetails</td><td>Ямар өгөгдөл дамжуулж байгаа нь ойлгомжтой.</td></tr><tr><td>id</td><td>userId</td><td>Яг юуны id юм бэ гэдэг нь ойлгомжтой.</td></tr><tr><td>info</td><td>movie</td><td>Props-ын утга тодорхой харагдана.</td></tr><tr><td>btnTxt</td><td>buttonText</td><td>Ийм цөөхөн үсэгтэй үгийг зүгээр л бүтэн биччих.</td></tr><tr><td>loading</td><td>isLoading</td><td>Үйл үг + нэр үр</td></tr><tr><td>onClick</td><td>onMovieCardClick</td><td>Хаана, яагаад ашиглаж байгаа нь ойлгомжтой.</td></tr></tbody></table>









