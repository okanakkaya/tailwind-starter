step-1
Bilgisayarda node yüklü olması lazım. Terminali aç node -v

step-2
vs code da teminali aç ve npm init -y 

step-3
npm install -D tailwindcss
npx tailwindcss init

step-4
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}

step-5
src dosyasını oluşturuyoruz. içerisine index.html dosyası,css ve img klasörlerini oluştur.

step-6
src ile aynı katmanda input.css dosyası oluştur ve içerisine aşağıdakileri ekle.
@tailwind base;
@tailwind components;
@tailwind utilities;

step-7
npx tailwindcss -i ./input.css -o ./src/css/styles.css --watch

step-8
index html başlangıç kodlarını ekle.

<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="./css/styles.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>

step-9
aşağıdaki komutu package.json dosyasında scriptlerin içerisine ekle. Projeyi çalıştırma komutudur.
"start": "npx tailwindcss -i ./input.css -o ./src/css/styles.css --watch"
npm run start şeklinde projeyi ayağa kaldırabiliriz.