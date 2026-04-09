# React JS — 1-6 darslar

## 1. React nima va nima uchun kerak

React  bu UI yani sahifadagi ko'rinadigan narsalarni qurishga yordam beradigan JS kutubxonasi. Framework emas, kutubxona fremeworkga vue js kiradi.


Oddiy JS bilan katta loyiha qilsang kod chalkashib ketadi. React esa kodni bo'laklarga — komponentlarga bo'ladi. Har bir tugma, header, card — bular alohida komponent. Kerak joyda chaqirib ishlatasan.

Yana bir yaxshi tomoni — Virtual DOM. Sahifa o'zgarganda hamma narsa yangilanmaydi, faqat o'zgargan qismi yangilanadi. Shu tezroq ishlaydi.

## 2. React asoslari

React ikki asosiy narsa bilan ishlaydi `react` va `react dom` paketlari.

`react` — komponent yozish uchun  
`react-dom` — o'sha komponentni haqiqiy sahifaga chiqarish uchun

React o'zi bitta `index.html` dagi bitta `div` ni topadi va hamma narsani shu ichiga soladi. Sahifada ko'p narsa ko'rinsa ham aslida hammasi shu bitta div ichida.



## 3. Yangi loyiha ochish

npx create-react-app loyiha-nomi

shu buyruq bilan hammasi tayyor bo'ladi. Keyin `npm start` deb ishga tushiramiz, brauzerda `localhost:5173` da ochiladi uni esa `localhost:3000` qilib olish mumkin.

`src` papkasi — kod yozadigan joying  
`public` papkasi — `index.html` va rasmlar shu yerda



## 4. JSX

JSX degani — JS ichida HTML yozish. Ko'rinishi HTML ga o'xshaydi lekin aslida JS.

Farqi shunda — `class` o'rniga `className` yoziladi, chunki `class` JS da band so'z.

JS kodi yozmoqchi bo'lsang uni `{}` ichiga olasan:

jsx
<p>Yosh: {18 + 5}</p>


JSX ni brauzer to'g'ridan to'g'ri tushunmaydi, Babel uni oddiy JS ga o'giradi. Biz buni ko'rmaymiz, o'zi ishlaydi.


## 5. Component va Element

Element — ekranga chiqadigan eng kichik narsa. Masalan bitta `<h1>` tegi.

Komponent — elementlarni qaytaradigan funksiya. Katta harf bilan boshlanadi.

jsx
function Salom() {
  return <h1>Salom!</h1>
}


Komponentga ma'lumot uzatmoqchi bo'lsang — props orqali uzatasan:

jsx
function Salom({ ism }) {
  return <h1>Salom, {ism}!</h1>
}

<Salom ism="Ali" />


Props ni komponent ichida o'zgartirib bo'lmaydi, faqat o'qiysan.

## 6. Loyiha strukturasi

Fayllarni tartibli saqlash kerak, loyiha kattalashganda qidirmaslik uchun.
src/
  components/   — kichik qayta ishlatiladigan komponentlar
  pages/        — to'liq sahifalar
  assets/       — rasmlar, ikonkalar
  App.jsx
  main.jsx
```

Har bir komponentni alohida faylga yozasan. Kerak joyda import qilib ishlatasan. Boshida bu ortiqcha ko'rinadi lekin loyiha o'sganda juda qulay bo'ladi.


*Sammi.ac — React JS kursi, 1-modul*