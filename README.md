# vue-app

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

------------



# Create Basic VUE-APP
## Instruksi Project Dari nol

# Vue CLI
[========]

- Pertama kita install vue CLI
	````bash
	# install with npm
	npm i -g @vue/cli @vue/cli-service-global

	# install with yarn
	yarn global add @vue/cli @vue/cli-service-global
	````
	Sekarang Vue CLI telah terinsal secara global, kita bisa menggunakan command vue dimana saja. 

- Kita akan menggunakan `vue create` untuk memulai project baru.
	```bash
	vue create vue-app
	```
	Akan muncul tampilan seperti ini, terdapat beberapa opsi untuk hal ini kita pilih `Manual select features`

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=auto&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=true&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=Vue%2520CLI%2520v4.5.11%250A%253F%2520Please%2520pick%2520a%2520preset%253A%250A%2520%2520Default%2520%28%255BVue%25202%255D%2520babel%252C%2520eslint%29%250A%2520%2520Default%2520%28Vue%25203%2520Preview%29%2520%28%255BVue%25203%255D%2520babel%252C%2520eslint%29%250A%253E%2520Manually%2520select%2520features"
  style="width: 549px; height: 240px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin"></iframe>

	Untuk sementara kita hanya centang `Choose Vue version`
<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=auto&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=true&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=Vue%2520CLI%2520v4.5.11%250A%253F%2520Please%2520pick%2520a%2520preset%253A%2520Manually%2520select%2520features%250A%253F%2520Check%2520the%2520features%2520needed%2520for%2520your%2520project%253A%250A%253E%28*%29%2520Choose%2520Vue%2520version%250A%2520%28%2520%29%2520Babel%250A%2520%28%2520%29%2520TypeScript%250A%2520%28%2520%29%2520Progressive%2520Web%2520App%2520%28PWA%29%2520Support%250A%2520%28%2520%29%2520Router%250A%2520%28%2520%29%2520Vuex%250A%2520%28%2520%29%2520CSS%2520Pre-processors%250A%2520%28%2520%29%2520Linter%2520%252F%2520Formatter%250A%2520%28%2520%29%2520Unit%2520Testing%250A%2520%28%2520%29%2520E2E%2520Testing"
  style="width: 549px; height: 432px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

	Disini kita akan menggunakan yang versi 2.x
	<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=auto&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=true&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=Vue%2520CLI%2520v4.5.11%250A%253F%2520Please%2520pick%2520a%2520preset%253A%2520Manually%2520select%2520features%250A%253F%2520Check%2520the%2520features%2520needed%2520for%2520your%2520project%253A%2520Choose%2520Vue%2520version%250A%253F%2520Choose%2520a%2520version%2520of%2520Vue.js%2520that%2520you%2520want%2520to%2520start%2520the%2520project%2520with%2520%28Use%2520arrow%2520keys%29%250A%253E%25202.x%250A%2520%25203.x%2520%28Preview%29"
  style="width: 549px; height: 360px; 9px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
	</iframe>
	
	Silahkan anda pilih letak config untuk Babel, ESlint, dll berada. Kalau saya lebih suka saya taruh di package.json
	<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=application%2Fx-sh&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=true&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253F%2520Where%2520do%2520you%2520prefer%2520placing%2520config%2520for%2520Babel%252C%2520ESLint%252C%2520etc.%253F%250A%2520%2520In%2520dedicated%2520config%2520files%250A%253E%2520In%2520package.json"
  style="width: 549px; height: 281px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
	</iframe>
	
	Setelah semua instalasi selesai, kita bisa berpindah ke direktori project yang sudah dibuat dan run project dengan perintah seperti dibawah ini:
	<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=auto&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=true&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=cd%2520vue-app%250A%250Anpm%2520run%2520serve%250A%2523%2520or%250Ayarn%2520serve"
  style="width: 549px; height: 281px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
	</iframe>
	
	Pada titik ini kita sudah selesai mempersiapkan semua yang dibutuhkan untuk membangun Vue aplikasi. jangan lupa tambahkan plugin Vetur untuk formatter dan highlight pada text editor anda dan juga install ekstensi Vue Devtools untuk memberi informasi tentang *components* - *state, method, data,* dll ketika anda *running* vue pada browser anda.


# Getting Started
Selamat kita sudah me-setting Vue boilerplate app. di projek ini terdapat `public` folder yang didalamnya terdapat `index.html`, dan `src` folder dengan `main.js` sebagai titik awal js. Disini juga kita diperkenalkan pula dengan `.vue` file, dengan komponen `HelloWorld.vue` dan `App.vue`.

## Titik Awal
Pada `main.js` disini membawa Vue dan *redering* App ke app div pada `index.html`. File ini tidak butuh diubah.
<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=javascript&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=import%2520Vue%2520from%2520%27vue%27%250Aimport%2520App%2520from%2520%27.%252FApp.vue%27%250A%250AVue.config.productionTip%2520%253D%2520false%250A%250Anew%2520Vue%28%257B%250A%2520%2520render%253A%2520function%2520%28h%29%2520%257B%2520return%2520h%28App%29%2520%257D%252C%250A%257D%29.%2524mount%28%27%2523app%27%29"
  style="width: 700px; height: 337px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

## Anatomi Vue
Ketika kita akan membuat suatu file `.vue`, selalu terdapat 3 tag yang pasti yaitu:
- `<template>`
- `<script>`
- `<style>`

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Ctemplate%253E%253C%252Ftemplate%253E%250A%250A%253Cscript%253E%250A%2520%2520export%2520default%2520%257B%250A%2520%2520%2520%2520name%253A%2520%27nama-komponen%27%252C%250A%2520%2520%257D%250A%253C%252Fscript%253E%250A%250A%253Cstyle%2520scoped%253E%253C%252Fstyle%253E"
  style="width: 700px; height: 356px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Setiap data logic pada setiap komponen akan berada pada tag `<script>`, seperti kita tahu `<style>` hanya digunakan untuk CSS, kita juga bisa gunakan `scoped` untuk mengaplikasikan style tersebut tidak secara global.

Karena tujuan dari pembelajaran kali ini adalah tentang fungsionalitas, bukan soal *styling*, saya akan menambahkan secara cepat `Skeleton` framework CSS pada `public/index.html` file untuk lebih memudahkan dalam *styling*.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=htmlmixed&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253C%21DOCTYPE%2520html%253E%250A%253Chtml%2520lang%253D%2522%2522%253E%250A%2520%2520%253Chead%253E%250A%2509%253C%21--%2520....%2520isi%2520header%2520--%253E%250A%2520%2520%2520%2520%253Clink%2520rel%253D%2522stylesheet%2522%2520href%253D%2522https%253A%252F%252Fcdnjs.cloudflare.com%252Fajax%252Flibs%252Fskeleton%252F2.0.4%252Fskeleton.min.css%2522%253E%250A%2520%2520%253C%252Fhead%253E%250A%2520%2520%253Cbody%253E%250A%2520%2520%2520%2520%253C%21--%2520....%2520isi%2520body%2520--%253E%250A%2520%2520%253C%252Fbody%253E%250A%253C%252Fhtml%253E"
  style="width: 700px; height: 375px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Putar musik lo-fi 🎧 dan mulai memasak 👨‍🍳.


# Creating a Component

Buat file dengan nama `MahasiswaTable.vue` du `src/components`. Kita akan membuat tabel dengan beberapa data statik seperti dibawah ini.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Ctemplate%253E%250A%2520%2520%253Cdiv%2520id%253D%2522mhs-table%2522%253E%250A%2520%2520%2520%2520%253Ctable%2520class%253D%2522u-full-width%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cthead%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctr%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Cth%253ENama%253C%252Fth%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Cth%253ENo%2520Induk%2520Mahasiswa%253C%252Fth%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Cth%253EEmail%253C%252Fth%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253C%252Ftr%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253C%252Fthead%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Ctbody%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctr%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctd%253EJonatan%2520Teofilus%253C%252Ftd%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctd%253E6876879890%253C%252Ftd%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctd%253Ejonatan.teofilus%2540gmail.com%253C%252Ftd%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253C%252Ftr%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctr%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctd%253EDwayne%2520Johnson%253C%252Ftd%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctd%253E0978769767%253C%252Ftd%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctd%253Edwayne150%2540gmail.com%253C%252Ftd%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253C%252Ftr%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253C%252Ftbody%253E%250A%2520%2520%2520%2520%253C%252Ftable%253E%250A%2520%2520%253C%252Fdiv%253E%250A%253C%252Ftemplate%253E%250A%250A%253Cscript%253E%250Aexport%2520default%2520%257B%250A%2509name%253A%2520%27mahasiswa-table%27%252C%250A%257D%250A%253C%252Fscript%253E%250A%250A%253Cstyle%2520scoped%253E%250A%250A%253C%252Fstyle%253E"
  style="width: 700px; height: 848px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Di Vue, import nama file akan menjadi PascalCase, seperti `MahasiswaTable` tapi ketika komponen tersebut digunakan pada `<template>`, akan berubah menjadi kebab-case, `<mahasiswa-table>`. Hal ini supaya kita bisa mengenali konvensi untuk masing-masing javascript dan HTML.

Kita export `mahasiswaTable` dan import ke `App.vue`. Pada waktu me-import, kita bisa menggunakan `@` sebagai referensi `src` folder. App.vue mengenali dan komponen tersebut bisa digunakan melalui `components` property. Jadi semua komponen yang dibutuhkan dalam satu `.vue` harus ditambahkan disana.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Ctemplate%253E%250A%2520%2520%253Cdiv%2520id%253D%2522app%2522%253E%250A%2520%2520%2520%2520%253Cdiv%2520class%253D%2522container%2522%253E%250A%2520%2520%2520%2520%2520%2520%253Ch1%253EMahasiswa%253C%252Fh1%253E%250A%2520%2520%2520%2520%2520%2520%253Cmahasiswa-table%252F%253E%250A%2520%2520%2520%2520%253C%252Fdiv%253E%250A%2520%2520%253C%252Fdiv%253E%250A%253C%252Ftemplate%253E%250A%250A%253Cscript%253E%250Aimport%2520MahasiswaTable%2520from%2520%27%2540%252Fcomponents%252FMahasiswaTable.vue%27%250Aexport%2520default%2520%257B%250A%2520%2520name%253A%2520%27App%27%252C%250A%2520%2520components%253A%2520%257B%250A%2520%2520%2520%2520MahasiswaTable%250A%2520%2520%257D%250A%257D%250A%253C%252Fscript%253E%250A%250A%253Cstyle%2520scoped%253E%250A%253C%252Fstyle%253E%250A"
  style="width: 700px; height: 602px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Akan tampil seperti ini:
####gambar review

Supaya data pada tabel menjadi dinamis, kita akan ubah menjadi array object. Jadi mari kita tambah method `data()` dan return array mahasiswa. kita juga menambahkan ID untuk setiap item agar membuatnya untuk dan teridentifikasi.

Sekarang kita memiliki data tersebut pada `App.vue`, tapi kita harus bawa data tersebut ke `MahasiswaTable`. Kita bisa melakukan hal itu dengan *passing* date sebagai properti. Sebuah atribut dengan *colon* `:` untuk mengirim data pada. `:` juga merupakan *shorthand* dari `v-bind`. Dalam kasus ini kita akan membawa array datamahasiswa.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Cmahasiswa-table%2520%253Adatamahasiswa%253D%2522datamahasiswa%2522%252F%253E%250A%253C%21--%2520atau%2520--%253E%250A%253Cmahasiswa-table%2520v-bind%253Adatamahasiswa%253D%2522datamahasiswa%2522%252F%253E"
  style="width: 700px; height: 243px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Saat ini pada sisi `MahasiswaTable`, kita ingin mengambil data tersebut, jadi kita harus membuat `props` attribute dengan nama `datamahasiswa`.

## Loops

Sekarang kita telah mendapatkan data tersebut, kita butuh mengulang data dan menampilkanya ke DOM. Kita bisa lakukan ini dengan menggunakan `v-for` attribute. Sekarang kita telah mendapatkan `datamahasiswa` di `MahasiswaTable` kita tampilkan per baris.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Ctemplate%253E%250A%2520%2520%253Cdiv%2520id%253D%2522mhs-table%2522%253E%250A%2520%2520%2520%2520%253Ctable%2520class%253D%2522u-full-width%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cthead%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctr%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Cth%253ENama%253C%252Fth%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Cth%253ENo%2520Induk%2520Mahasiswa%253C%252Fth%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Cth%253EEmail%253C%252Fth%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253C%252Ftr%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253C%252Fthead%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Ctbody%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctr%2520v-for%253D%2522mahasiswa%2520in%2520datamahasiswa%2522%2520%253Akey%253D%2522mahasiswa.id%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctd%253E%257B%257B%2520mahasiswa.nama%2520%257D%257D%253C%252Ftd%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctd%253E%257B%257B%2520mahasiswa.npm%2520%257D%257D%253C%252Ftd%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctd%253E%257B%257B%2520mahasiswa.email%2520%257D%257D%253C%252Ftd%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253C%252Ftr%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253C%252Ftbody%253E%250A%2520%2520%2520%2520%253C%252Ftable%253E%250A%2520%2520%253C%252Fdiv%253E%250A%253C%252Ftemplate%253E"
  style="width: 700px; height: 564px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>



# Form

Kita sekarang membuat form tambah mahasiswa. 

Buat `MahasiswaForm.vue` dan atur field nama, npm, email dan juga `button` submit. Juga buat data object mahasiswa dengan nama, npm dan juga email.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Ctemplate%253E%250A%2520%2520%253Cform%253E%250A%2520%2520%2520%2520%253Cdiv%2520class%253D%2522row%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Clabel%2520for%253D%2522inputNama%2522%253ENama%2520Mahasiswa%253C%252Flabel%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cinput%2520class%253D%2522u-full-width%2522%2520type%253D%2522text%2522%2520placeholder%253D%2522Nama%2520Mahasisiwa%2522%2520id%253D%2522inputNama%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Clabel%2520for%253D%2522inputNpm%2522%253ENomer%2520Induk%2520Mahasiswa%253C%252Flabel%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cinput%2520class%253D%2522u-full-width%2522%2520type%253D%2522text%2522%2520placeholder%253D%2522Nomor%2520Induk%2520Mahasiswa%2522%2520id%253D%2522inputNpm%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Clabel%2520for%253D%2522inputNama%2522%253EEmail%2520Mahasiswa%253C%252Flabel%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cinput%2520class%253D%2522u-full-width%2522%2520type%253D%2522email%2522%2520placeholder%253D%2522Email%2520Mahasisiwa%2522%2520id%253D%2522inputEmail%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cbutton%2520class%253D%2522button-primary%2522%253EAdd%2520Mahasiswa%253C%252Fbutton%253E%250A%2520%2520%2520%2520%253C%252Fdiv%253E%250A%2520%2520%253C%252Fform%253E%250A%253C%252Ftemplate%253E%250A%250A%253Cscript%253E%250Aexport%2520default%2520%257B%250A%2520%2520%2520%2520data%28%29%2520%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520return%2520%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520mahasiswa%253A%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520nama%253A%27%27%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520npm%253A%27%27%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520email%253A%27%27%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%257D%250A%2520%2520%2520%2520%2520%2520%2520%2520%257D%250A%2520%2520%2520%2520%257D%252C%250A%257D%250A%253C%252Fscript%253E%250A%250A%253Cstyle%2520scoped%253E%250A%2520%2520form%2520%257B%250A%2520%2520%2520%2520margin-bottom%253A%25202rem%253B%250A%2520%2520%257D%250A%253C%252Fstyle%253E"
  style="width: 700px; height: 810px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>


Kita juga menambahkan beberapa baris code pada `App.vue`

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Ctemplate%253E%250A%2520%2520%253Cdiv%2520id%253D%2522app%2522%253E%250A%2520%2520%2520%2520%253Cdiv%2520class%253D%2522container%2522%253E%250A%2520%2520%2520%2520%2520%2520%253Ch1%253EMahasiswa%253C%252Fh1%253E%250A%2520%2520%2520%2520%2520%2520%253Cmahasiswa-form%252F%253E%250A%2520%2520%2520%2520%2520%2520%253Cmahasiswa-table%2520%253Adatamahasiswa%253D%2522datamahasiswa%2522%252F%253E%250A%2520%2520%2520%2520%253C%252Fdiv%253E%250A%2520%2520%253C%252Fdiv%253E%250A%253C%252Ftemplate%253E%250A%250A%253Cscript%253E%250Aimport%2520MahasiswaTable%2520from%2520%27%2540%252Fcomponents%252FMahasiswaTable.vue%27%250Aimport%2520MahasiswaForm%2520from%2520%27%2540%252Fcomponents%252FmahasiswaForm.vue%27%250Aexport%2520default%2520%257B%250A%2520%2520name%253A%2520%27App%27%252C%250A%2520%2520components%253A%2520%257B%250A%2520%2520%2520%2520MahasiswaTable%252C%250A%2520%2520%2520%2520MahasiswaForm%250A%2520%2520%257D%252C%250A%2520%2520data%28%29%2520%257B%250A%2520%2520%2520%2520%252F%252F...%250A%2520%2520%257D%252C%250A%257D%250A%253C%252Fscript%253E%250A%250A%253Cstyle%2520scoped%253E%250A%253C%252Fstyle%253E%250A"
  style="width: 700px; height: 715px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Sekarang gimana caranya mendapatkan data dan mengirimkannya ke Vue component state. Untuk itu kita gunakan `v-model`. `v-model` suatu *sytactic sugar* built-in Vue untuk mengubah input value ketika ada event `onchange`.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Ctemplate%253E%250A%2520%2520%253Cform%253E%250A%2520%2520%2520%2520%253Cdiv%2520class%253D%2522row%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Clabel%2520for%253D%2522inputNama%2522%253ENama%2520Mahasiswa%253C%252Flabel%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cinput%2520v-model%253D%2522mahasiswa.nama%2522%2520class%253D%2522u-full-width%2522%2520type%253D%2522text%2522%2520placeholder%253D%2522Nama%2520Mahasisiwa%2522%2520id%253D%2522inputNama%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Clabel%2520for%253D%2522inputNpm%2522%253ENomer%2520Induk%2520Mahasiswa%253C%252Flabel%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cinput%2520v-model%253D%2522mahasiswa.npm%2522%2520class%253D%2522u-full-width%2522%2520type%253D%2522text%2522%2520placeholder%253D%2522Nomor%2520Induk%2520Mahasiswa%2522%2520id%253D%2522inputNpm%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Clabel%2520for%253D%2522inputNama%2522%253EEmail%2520Mahasiswa%253C%252Flabel%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cinput%2520v-model%253D%2522mahasiswa.email%2522%2520class%253D%2522u-full-width%2522%2520type%253D%2522email%2522%2520placeholder%253D%2522Email%2520Mahasisiwa%2522%2520id%253D%2522inputEmail%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cbutton%2520class%253D%2522button-primary%2522%253EAdd%2520Mahasiswa%253C%252Fbutton%253E%250A%2520%2520%2520%2520%253C%252Fdiv%253E%250A%2520%2520%253C%252Fform%253E%250A%253C%252Ftemplate%253E"
  style="width: 700px; height: 488px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Sekarang kita bisa tambahkan ini, kita bisa lihati di Vue DevTools ketika *state* pada komponen berubah. 
Kita tinggal submit lalu update ke parent `(App)` state dengan object mahasiswa baru.


# Event listeners

Untuk submit form kita tambahkan atribut `v-on:submit` atau kita bisa gunakan `@submit` untuk shorthand pada tag `<form>`. ini sama dengan event `@click/v-on:click`. Event submit juga memiliki `prevent` yang difungsikan untuk mematikan method GET/POST yang secara default sudah disediakan oleh form.

Mari kita tambah script ini ke form, dan juga buat method submitMahasiswa.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Cform%2520%2540submit.prevent%253D%2522submitMahasiswa%2522%253E%253C%252Fform%253E"
  style="width: 700px; height: 205px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

# Methods

Saat ini kita membuat method pertama pada component. Dibawah `data()`, kita bisa buat object `methods`, dimana akan menampung semua custom method yang kita buat. mari kita buat `submitMahasiswa` disana.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Cscript%253E%250Aexport%2520default%2520%257B%250A%2520%2520%2520%2520data%28%29%2520%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520return%2520%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520mahasiswa%253A%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520nama%253A%27%27%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520npm%253A%27%27%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520email%253A%27%27%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%257D%250A%2520%2520%2520%2520%2520%2520%2520%2520%257D%250A%2520%2520%2520%2520%257D%252C%250A%2520%2520%2520%2520methods%253A%2520%257B%250A%2520%2520%2520%2520%2520%2520submitMahasiswa%28%29%2520%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520console.log%28%2522test%2520submited%2522%29%250A%2520%2520%2520%2520%2520%2520%257D%250A%2520%2520%2520%2520%257D%252C%250A%257D%250A%253C%252Fscript%253E"
  style="width: 700px; height: 526px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

# Emitting events

Sekarang kita coba submit form, kita akan melihat message log di console, lalubagaimana caranya kita mengirimkan data ke parent `App` sekarang? tentunya kita bisa melakukan hal tersebut dengan `$emit`

Emit mengirim nama event dan data ke parent component, seperti ini:

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=this.%2524emit%28%27nama-emit-event%27%252C%2520dataPass%29"
  style="width: 700px; height: 205px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>


pada case kita, kita akan buat event dengan nama `add:mahasiswa` dan membawa data `this.mahasiswa`

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=submitMahasiswa%28%29%2520%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520this.%2524emit%28%2522add%253Amahasiswa%2522%252Cthis.mahasiswa%29%250A%257D"
  style="width: 700px; height: 243px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Ketika sudah ditambahakan, klik untuk add form lalu ke Vue DevTools. kita akan lihat notifikasi untuk event baru, dan akan memberi tahu kuta tentang nama, source, dan payload, dimana pada kasus ini object terbuat.

## Menerima Event dari child component

hal pertama yang harus dilakukan adalah membuat supaya `mahasiswa-form` untuk me-handle event yang di-emmit untuk memanggil ke method baru. contoh seperti ini:

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Ccomponent%2520%2540name-of-emitted-event%253D%2522methodToCallOnceEmitted%2522%253E%253C%252Fcomponent%253E"
  style="width: 700px; height: 205px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Mari kita tambah ke App.vue.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Cmahasiswa-form%2520%2540add%253Amahasiswa%253D%2522addMahasiswa%2522%252F%253E"
  style="width: 700px; height: 205px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Kita hanya perlu membuat method `addMahasiswa` di `App.vue`, dimana memodifikasi array `datamahasiswa` dengan menambah item baru kedalamnya.
kode dibawah adalah untuk mendapatkan `id` mahasiswa baru berdasarkan nomer item array. Pada database sebenarnya, `id` sudah tergenerate secara unik atau *auto increment*.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=addMahasiswa%28mahasiswa%29%2520%257B%250A%250A%2520%2520const%2520lastId%2520%253D%2520this.datamahasiswa.length%2520%253E%25200%253F%2520this.datamahasiswa%255Bthis.datamahasiswa.length%2520-%25201%255D.id%253A%25200%2520%253B%250A%2520%2520const%2520id%2520%253D%2520lastId%2520%252B%25201%253B%250A%2520%2520%252F%252F%2520Using%2520spread%2520untuk%2520will%2520clone%2520your%2520object.%250A%2520%2520const%2520newMahasiswa%2520%253D%2520%257B%2520...mahasiswa%252C%2520id%2520%257D%253B%250A%2520%2520%252F%252F%2520spread%2520untuk%2520mengulang%250A%2520%2520this.datamahasiswa%2520%253D%2520%255B...this.datamahasiswa%252C%2520newMahasiswa%255D%253B%250A%257D"
  style="width: 700px; height: 356px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>


sekarang dengan ini, kita sudah bisa add mahasiswa baru.  Nggak sampai disini karena ini hanya front end dan tidak terkoneksi dengan database.


# Form Validation

Kebutuhan validasi adalah sebagai berikut:
- Menampilkan success message jika semua terkirim.
- Menampilkan error message jika terdapat input yang salah atau kosong.
- Highlight pada input yang tidak valid.
- Bersihkan semua input setelah form telah tersubmit dengan baik.
- Fokus pada item pertama jika sukses.

## Computed properties

Di Vue, kita bisa menggunakan **computed properties**, dimana suatu fungsi secara otomatis melakukan penghitungan/menjalankan ketika sesuatu berubah. Disini saya coba untuk membuat *basic check* validasi untuk memastikan field tidak kosong untuk semua input field.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=computed%253A%2520%257B%250A%2520%2520invalidNama%28%29%2520%257B%250A%2520%2520%2520%2520return%2520this.mahasiswa.nama%2520%253D%253D%253D%2520%27%27%250A%2520%2520%257D%252C%250A%2520%2520invalidNpm%28%29%2520%257B%250A%2520%2520%2520%2520return%2520this.mahasiswa.npm%2520%253D%253D%253D%2520%27%27%250A%2520%2520%257D%252C%250A%2520%2520invalidEmail%28%29%2520%257B%250A%2520%2520%2520%2520return%2520this.mahasiswa.email%2520%253D%253D%253D%2520%27%27%250A%2520%2520%257D%252C%250A%257D%252C"
  style="width: 700px; height: 394px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Kita juga membutuhkan `submitting` *state* untuk mengecek apakah form sudah tersubmit, `error` *state*  jika sesuatu salah dan `success` *state* jika form input benar.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=data%28%29%2520%257B%250A%2520%2520%2520%2520return%2520%257B%250A%2520%2520%2520%2520%2520%2520submitting%253A%2520false%252C%250A%2520%2520%2520%2520%2520%2520error%253A%2520false%252C%250A%2520%2520%2520%2520%2520%2520success%253A%2520false%252C%250A%2520%2520%2520%2520%2520%2520mahasiswa%253A%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520nama%253A%27%27%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520npm%253A%27%27%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520email%253A%27%27%250A%2520%2520%2520%2520%2520%2520%257D%250A%2520%2520%2520%2520%257D%250A%257D%252C"
  style="width: 700px; height: 413px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Fungsi submit pertama akan mereset ulang state baik itu succes atau error yang telah terseting, mulai submit, setelah itu cek semua method `computed` dan jika terdapat return *true*, maka error state akan diset. Jika tida kita bisa submit, dan mengatur state sukses dan semua state kembali seperti semula.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=methods%253A%2520%257B%250A%2520%2520submitMahasiswa%28%29%2520%257B%250A%2520%2520%2520%2520%252F%252F%2520set%2520state%2520menjadi%2520tersubmit%250A%2520%2520%2520%2520this.submitting%2520%253D%2520true%250A%2520%2520%2520%2520%252F%252F%2520bersihkan%2520terlebih%2520dahulu%2520state%2520error%2520%2526%2520success%250A%2520%2520%2520%2520this.clearStatus%28%29%250A%250A%2520%2520%2520%2520%252F%252F%2520panggil%2520setiap%2520computed%2520fungsi%2520untuk%2520validasi%250A%2520%2520%2520%2520if%2520%28this.invalidNama%2520%257C%257C%2520this.invalidNpm%2520%257C%257C%2520this.invalidEmail%29%2520%257B%250A%2520%2520%2520%2520%2520%2520this.error%2520%253D%2520true%250A%2520%2520%2520%2520%2520%2520return%250A%2520%2520%2520%2520%257D%250A%250A%2520%2520%2520%2520%252F%252F%2520emit%2520ke%2520parent%250A%2520%2520%2520%2520this.%2524emit%28%2522add%253Amahasiswa%2522%252Cthis.mahasiswa%29%250A%250A%2520%2520%2520%2520%252F%252F%2520kosongkan%2520kembali%2520obj%2520mahasiswa%250A%2520%2520%2520%2520this.clearMahasiswa%28%29%250A%250A%2520%2520%2520%2520%252F%252F%2520set%2520sukses%250A%2520%2520%2520%2520this.error%2520%253D%2520false%250A%2520%2520%2520%2520this.success%2520%253D%2520true%250A%2520%2520%2520%2520%252F%252F%2520set%2520status%2520submit%2520jadi%2520false%250A%2520%2520%2520%2520this.submitting%2520%253D%2520false%250A%2520%2520%257D%252C%250A%2520%2520clearStatus%28%29%2520%257B%250A%2520%2520%2520%2520this.success%2520%253D%2520false%250A%2520%2520%2520%2520this.error%2520%253D%2520false%250A%2520%2520%257D%252C%250A%2520%2520clearMahasiswa%28%29%257B%250A%2520%2520%2520%2520this.mahasiswa%2520%253D%2520%257B%250A%2520%2520%2520%2520%2520%2520nama%253A%27%27%252C%250A%2520%2520%2520%2520%2520%2520npm%253A%27%27%252C%250A%2520%2520%2520%2520%2520%2520email%253A%27%27%250A%2520%2520%2520%2520%257D%250A%2520%2520%257D%250A%257D%252C"
  style="width: 700px; height: 885px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Saya juga tambahkan bebarapa baris CSS untuk kondisi success state dan error state.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Cstyle%2520scoped%253E%250A%2520%2520form%2520%257B%250A%2520%2520%2520%2520margin-bottom%253A%25202rem%253B%250A%2520%2520%257D%250A%2520%2520%250A%2520%2520%255Bclass*%253D%27-message%27%255D%2520%257B%250A%2520%2520%2520%2520font-weight%253A%2520500%253B%250A%2520%2520%257D%250A%250A%2520%2520.error-message%2520%257B%250A%2520%2520%2520%2520color%253A%2520%2523d33c40%253B%250A%2520%2520%257D%250A%250A%2520%2520.success-message%2520%257B%250A%2520%2520%2520%2520color%253A%2520%252332a95d%253B%250A%2520%2520%257D%250A%250A%2520%2520input.has-error%2520%257B%250A%2520%2520%2520%2520border%253A%25201.5px%2520solid%2520%2523d33c40%253B%253B%250A%2520%2520%257D%250A%253C%252Fstyle%253E"
  style="width: 700px; height: 583px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Akhirnya kita telah mengatur form. Jika form tersubmit dan satu dari antara computed preoperty tidak valid, kita akan set class `has-error` pada input. Gunakan `:class=` untuk memastikan bahwa class akan diterapkan melalui Javascript. Kita juga pastikan pesan success dan error tertampil di atas form.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Cform%2520%2540submit.prevent%253D%2522submitMahasiswa%2522%253E%250A%2520%2520%253Cdiv%2520class%253D%2522row%2522%253E%250A%2520%2520%2520%2520%2520%2520%253Clabel%2520for%253D%2522inputNama%2522%253ENama%2520Mahasiswa%253C%252Flabel%253E%250A%2520%2520%2520%2520%2520%2520%253Cinput%2520v-model%253D%2522mahasiswa.nama%2522%2520class%253D%2522u-full-width%2522%2520%253Aclass%253D%2522%257B%2520%27has-error%27%253A%2520submitting%2520%2526%2526%2520invalidNama%2520%257D%2522%2520type%253D%2522text%2522%2520placeholder%253D%2522Nama%2520Mahasisiwa%2522%2520id%253D%2522inputNama%2522%253E%250A%250A%2520%2520%2520%2520%2520%2520%253Clabel%2520for%253D%2522inputNpm%2522%253ENomer%2520Induk%2520Mahasiswa%253C%252Flabel%253E%250A%2520%2520%2520%2520%2520%2520%253Cinput%2520v-model%253D%2522mahasiswa.npm%2522%2520class%253D%2522u-full-width%2522%2520%253Aclass%253D%2522%257B%2520%27has-error%27%253A%2520submitting%2520%2526%2526%2520invalidNpm%2520%257D%2522%2520type%253D%2522text%2522%2520placeholder%253D%2522Nomor%2520Induk%2520Mahasiswa%2522%2520id%253D%2522inputNpm%2522%253E%250A%250A%2520%2520%2520%2520%2520%2520%253Clabel%2520for%253D%2522inputNama%2522%253EEmail%2520Mahasiswa%253C%252Flabel%253E%250A%2520%2520%2520%2520%2520%2520%253Cinput%2520v-model%253D%2522mahasiswa.email%2522%2520class%253D%2522u-full-width%2522%2520%253Aclass%253D%2522%257B%2520%27has-error%27%253A%2520submitting%2520%2526%2526%2520invalidEmail%2520%257D%2522%2520type%253D%2522email%2522%2520placeholder%253D%2522Email%2520Mahasisiwa%2522%2520id%253D%2522inputEmail%2522%253E%250A%250A%2520%2520%2520%2520%2520%2520%253Cp%2520v-if%253D%2522error%2520%2526%2526%2520submitting%2522%2520class%253D%2522error-message%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%25E2%259D%2597Isi%2520file%2520yang%2520dibutuhkan%250A%2520%2520%2520%2520%2520%2520%253C%252Fp%253E%250A%2520%2520%2520%2520%2520%2520%253Cp%2520v-if%253D%2522success%2522%2520class%253D%2522success-message%2522%253E%25E2%259C%2585%2520Sukses%2520menambahkan%2520mahasiswa.%253C%252Fp%253E%250A%250A%2520%2520%2520%2520%2520%2520%253Cbutton%2520class%253D%2522button-primary%2522%253EAdd%2520Mahasiswa%253C%252Fbutton%253E%250A%2520%2520%253C%252Fdiv%253E%250A%253C%252Fform%253E"
  style="width: 700px; height: 602px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>


# Delete

Form sudah selesai, sekarang tinggal update dan delete. Hal pertama yang akan kita kerjakan yaitu menambahkan baris `aksi`, dan button untuk edit dan delete.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Ctemplate%253E%250A%2520%2520%253Cdiv%2520id%253D%2522mhs-table%2522%253E%250A%2520%2520%2520%2520%253Ctable%2520class%253D%2522u-full-width%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cthead%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctr%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Cth%253ENama%253C%252Fth%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Cth%253ENo%2520Induk%2520Mahasiswa%253C%252Fth%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Cth%253EEmail%253C%252Fth%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Cth%253EAksi%253C%252Fth%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253C%252Ftr%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253C%252Fthead%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Ctbody%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctr%2520v-for%253D%2522mahasiswa%2520in%2520datamahasiswa%2522%2520%253Akey%253D%2522mahasiswa.id%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctd%253E%257B%257B%2520mahasiswa.nama%2520%257D%257D%253C%252Ftd%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctd%253E%257B%257B%2520mahasiswa.npm%2520%257D%257D%253C%252Ftd%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctd%253E%257B%257B%2520mahasiswa.email%2520%257D%257D%253C%252Ftd%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Ctd%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Cbutton%253Eedit%253C%252Fbutton%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253Cbutton%253Edelete%253C%252Fbutton%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253C%252Ftd%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%2520%253C%252Ftr%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253C%252Ftbody%253E%250A%2520%2520%2520%2520%253C%252Ftable%253E%250A%2520%2520%253C%252Fdiv%253E%250A%253C%252Ftemplate%253E%250A%250A%253Cscript%253E%250Aexport%2520default%2520%257B%250A%2520%2520%2520%2520props%253A%255B%2522datamahasiswa%2522%255D%252C%250A%257D%250A%253C%252Fscript%253E%250A%250A%253Cstyle%2520scoped%253E%250A%2520%2520%2520%2520button%2520%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520margin%253A2px%250A%2520%2520%2520%2520%257D%250A%253C%252Fstyle%253E"
  style="width: 700px; height: 885px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

kita akan emit dan membawa id untuk memanggil fungsi `deleteMahasiswa` yang nanti akan kita buat pada parent.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Cbutton%2520%2540click%253D%2522%2524emit%28%27delete%253Amahasiswa%27%252C%2520mahasiswa.id%29%2522%253EDelete%253C%252Fbutton%253E"
  style="width: 700px; height: 205px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

kembali ke `App.vue`, kita telah menambah event aksi on delete-mahasiswa pada `mahasiswa-table`, tambahakan fungsi untuk menghandler event tersebut.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Cmahasiswa-table%2520%2540delete%253Amahasiswa%253D%2522deleteMahasiswa%2522%2520%253Adatamahasiswa%253D%2522datamahasiswa%2522%252F%253E"
  style="width: 700px; height: 205px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

dan kita lakukan filter array dengan menambahkan method `deleteMahasiswa` dan dengan logika seperti dibawah.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=deleteMahasiswa%28id%29%257B%250A%2520%2520this.datamahasiswa%2520%253D%2520this.datamahasiswa.filter%28mahasiswa%2520%253D%253E%2520mahasiswa.id%2520%21%253D%253D%2520id%29%250A%257D"
  style="width: 700px; height: 243px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Sekarang kita bisa hapus item. mari kita buat pesan untuk memberi info data mahasiswa kosong jika array `datamahasiswa` kosong.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Cdiv%2520id%253D%2522mhs-table%2522%253E%250A%2520%2520%2520%2520%253Cp%2520v-if%253D%2522datamahasiswa%2520%253C%25201%2522%253E%2520data%2520mahasiswa%2520kosong%253C%252Fp%253E%250A%2520%2520%2520%2520%253Ctable%2520v-else%2520class%253D%2522u-full-width%2522%253E%250A%2509%2509...%250A%2520%2520%2520%2520%253C%252Ftable%253E%250A%253C%252Fdiv%253E"
  style="width: 700px; height: 299px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Kita telah selesai menghapus item mahasiswa.


# Edit item

Editing is a little more complex than deleting. The setup from App.vue is simple though, so we'll do that first. Just add the edit:employee event that we'll be making:

Edit data seding lebih *tricky* dibandingkan dengan delete. Hal pertama yang dilakukan yaitu kita tambah event `edit:mahasiswa` dan kita juga buatkan method untuk menghadle event tersebut dengan nama `editMahasiswa` sama seperti delete.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Cmahasiswa-table%2520%250A%2520%2520%2540delete%253Amahasiswa%253D%2522deleteMahasiswa%2522%2520%250A%2520%2520%2540edit%253Amahasiswa%253D%2522editMahasiswa%2522%250A%2520%2520%253Adatamahasiswa%253D%2522datamahasiswa%2522%252F%253E"
  style="width: 700px; height: 262px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

dan pada method `editMahasiswa`, kita akan ambil data dari array berdasarkan id lalu kita update.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=editMahasiswa%28id%252C%2520updatemahasiswa%29%257B%250A%2520%2520%2520%2520%2520%2520this.datamahasiswa%2520%253D%2520this.datamahasiswa.map%28mahasiswa%2520%253D%253E%2520mahasiswa.id%2520%253D%253D%2520id%2520%253F%2520updatemahasiswa%2520%253A%2520mahasiswa%29%253B%250A%257D"
  style="width: 700px; height: 262px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Cukup mudah.

Sekarang kembali ke `MahasiswaTable.vue`, kita ingin buat "edit mode" enable ketika button terklik.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Cbutton%2520%2540click%253D%2522editMode%28mahasiswa.id%29%2522%253EEdit%253C%252Fbutton%253E"
  style="width: 700px; height: 205px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

kita akan membuat editing state dan akan get dan set id pada row yang sedang pada posisi edited ketika `editMode` enabled. `MahasiswaTable` memiliki local method `editMahasiswa` yang memiliki fungsi untuk emit `edit:mahasiswa` di App jika semua value field tidak kosong, proses kedua yaitu kita reset edit state.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=data%28%29%2520%257B%250A%2520%2520%2520%2520return%2520%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520editing%253A%2520null%252C%250A%2520%2520%2520%2520%257D%250A%257D%252C%250Amethods%253A%2520%257B%250A%2520%2520%2520%2520editMode%28id%29%2520%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520this.editing%2520%253D%2520id%250A%2520%2520%2520%2520%257D%252C%250A%2520%2520%2520%2520editMahasiswa%28mahasiswa%29%2520%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520if%2520%28mahasiswa.nama%2520%253D%253D%253D%2520%27%27%2520%257C%257C%2520mahasiswa.email%2520%253D%253D%253D%2520%27%27%2520%257C%257C%2520mahasiswa.npm%2520%253D%253D%253D%2520%27%27%29%2520return%250A%2520%2520%2520%2520%2520%2520%2520%2520this.%2524emit%28%27edit%253Amahasiswa%27%252C%2520mahasiswa.id%252C%2520mahasiswa%29%250A%2520%2520%2520%2520%2520%2520%2520%2520this.editing%2520%253D%2520null%250A%2520%2520%2520%2520%257D%250A%257D"
  style="width: 700px; height: 470px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

untuk membuat editable, kita akan cek data `editing === mahasiswa.id` kalau sama pada baris tersebut, maka input akan ditampilkan. kita juga tambahkan button `cancel` untuk mebatalkan edit dan set `editing` menjadi null.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=%253Ctr%2520v-for%253D%2522mahasiswa%2520in%2520datamahasiswa%2522%2520%253Akey%253D%2522mahasiswa.id%2522%253E%250A%2520%2520%2520%2520%253Ctd%2520v-if%253D%2522editing%2520%253D%253D%253D%2520mahasiswa.id%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cinput%2520type%253D%2522text%2522%2520v-model%253D%2522mahasiswa.nama%2522%2520placeholder%253D%2522Nama%2520Mahasiswa%2522%252F%253E%250A%2520%2520%2520%2520%253C%252Ftd%253E%250A%2520%2520%2520%2520%253Ctd%2520v-else%253E%257B%257B%2520mahasiswa.nama%2520%257D%257D%253C%252Ftd%253E%250A%2520%2520%2520%2520%253Ctd%2520v-if%253D%2522editing%2520%253D%253D%253D%2520mahasiswa.id%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cinput%2520type%253D%2522text%2522%2520v-model%253D%2522mahasiswa.npm%2522%2520placeholder%253D%2522Nomor%2520Induk%2520Mahasiswa%2522%252F%253E%250A%2520%2520%2520%2520%253C%252Ftd%253E%250A%2520%2520%2520%2520%253Ctd%2520v-else%253E%257B%257B%2520mahasiswa.npm%2520%257D%257D%253C%252Ftd%253E%250A%2520%2520%2520%2520%253Ctd%2520v-if%253D%2522editing%2520%253D%253D%253D%2520mahasiswa.id%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cinput%2520type%253D%2522email%2522%2520v-model%253D%2522mahasiswa.email%2522%2520placeholder%253D%2522Email%2520Mahasiswa%2522%252F%253E%250A%2520%2520%2520%2520%253C%252Ftd%253E%250A%2520%2520%2520%2520%253Ctd%2520v-else%253E%257B%257B%2520mahasiswa.email%2520%257D%257D%253C%252Ftd%253E%250A%2520%2520%2520%2520%253Ctd%2520v-if%253D%2522editing%2520%253D%253D%253D%2520mahasiswa.id%2522%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cbutton%2520class%253D%2522button-primary%2522%2520%2540click%253D%2522editMahasiswa%28mahasiswa%29%2522%253ESave%253C%252Fbutton%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cbutton%2520%2540click%253D%2522editing%2520%253D%2520null%2522%253ECancel%253C%252Fbutton%253E%250A%2520%2520%2520%2520%253C%252Ftd%253E%250A%2520%2520%2520%2520%253Ctd%2520v-else%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cbutton%2520%2540click%253D%2522editMode%28mahasiswa.id%29%2522%253EEdit%253C%252Fbutton%253E%250A%2520%2520%2520%2520%2520%2520%2520%2520%253Cbutton%2520%2540click%253D%2522%2524emit%28%27delete%253Amahasiswa%27%252Cmahasiswa.id%29%2522%253Edelete%253C%252Fbutton%253E%250A%2520%2520%2520%2520%253C%252Ftd%253E%250A%253C%252Ftr%253E"
  style="width: 700px; height: 602px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

edit telah berhasil, tetapi masih ada masalah yaitu ketika `cancel` data tidak kembali seperti sebelum teredit. Maka dari itu kita butuh caching data mahasiswa sebelu diedit.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=editMode%28mahasiswa%29%2520%257B%250A%2520%2520%2520%2520this.cachemahasiswa%2520%253D%2520%257B...mahasiswa%257D%250A%2520%2520%2520%2520this.editing%2520%253D%2520mahasiswa.id%250A%257D%252C%250AcancelEdit%28mahasiswa%29%257B%250A%2520%2520%2520%2520Object.assign%28mahasiswa%252C%2520this.cachemahasiswa%29%250A%2520%2520%2520%2520this.editing%2520%253D%2520null%250A%257D"
  style="width: 700px; height: 337px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

saat ini kita telah selesai CRUD data mock, namun ketika dir real produksi app akan membuat API call ke back end database. kita akan coba buat.



# Asynchronous REST API

kita akan mengubah data mock dengan real API dan kita akan buat POST, PUT, dan DELETE request. Disini sudah tersedia APInya kita tinggal panggil.

Method asynchronous dengan `async/await` dan menggunakan `try/catch` blok seperti contoh dibawah ini.

sebenarnya untuk `Fetch API` sendiri sudah banyak opsi library node yang terkenal dan bisa digunakan seperti `Axios` dll. Namun disini saya hanya menggunakan `Fetch`, fetch merupakan bawaan dari javascript untuk async fetch API dan alasan lain yaitu karena tidak perlu menginstall depedensi dan tujuan sampel.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=async%2520asynchronousMethod%28%29%2520%257B%250A%2520%2520try%2520%257B%250A%2520%2520%2520%2520const%2520response%2520%253D%2520await%2520fetch%28%27url%27%29%250A%2520%2520%2520%2520const%2520data%2520%253D%2520await%2520response.json%28%29%250A%250A%2520%2520%2520%2520%252F%252F%2520do%2520something%2520with%2520%2560data%2560%250A%2520%2520%257D%2520catch%2520%28error%29%2520%257B%250A%2520%2520%2520%2520%252F%252F%2520do%2520something%2520with%2520%2560error%2560%250A%2520%2520%257D%250A%257D"
  style="width: 700px; height: 375px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

## Lifecycle methods

Ketika GET request, kita akan menghapus semua data array mahasiswa yang kita punya, lalu mengganti data tersebut dengan get dari API. Kita panggil GET pada saat vue `mounted` lifecycle method.

kenapa pada saat `mounted`?. Mounted dijalankan ketika component semua sudah terisi ke DOM. ini adalah cara yang biasa dilakukan ketika ingin menampilkan data dari API.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=export%2520default%2520%257B%250A%2520%2520name%253A%2520%27App%27%252C%250A%2520%2520components%253A%2520%257B%250A%2520%2520%2520%2520MahasiswaTable%252C%250A%2520%2520%2520%2520MahasiswaForm%250A%2520%2520%257D%252C%250A%2520%2520data%28%29%2520%257B%250A%2509...%250A%2520%2520%257D%252C%250A%2520%2520mounted%28%29%2520%257B%250A%2520%2520%2520%2520this.getMahasiswa%28%29%250A%2520%2520%257D%252C%250A%2520%2520methods%253A%2520%257B%250A%2509...%250A%2520%2520%257D%250A%257D"
  style="width: 700px; height: 488px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

mengatur CORS untuk request ke localhost. Buat file `Vue.config.js` tambahkan obj `proxy` pada direktori root project atau jika sudah ada silahkan dimodifikasi seperti di bawah.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=module.exports%2520%253D%2520%257B%250A%2520%2520devServer%253A%2520%257B%250A%2520%2520%2520%2520proxy%253A%2520%257B%250A%2520%2520%2520%2520%2520%2520%27%252Fapi%27%253A%2520%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520target%253A%2520%27http%253A%252F%252Flocalhost%253A8008%27%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520ws%253A%2520true%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520changeOrigin%253A%2520true%252C%250A%2520%2520%2520%2520%2520%2520%257D%252C%250A%2520%2520%2520%2520%257D%252C%250A%2520%2520%257D%252C%250A%257D%253B%250A"
  style="width: 700px; height: 413px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

### GET
Mengambil data.

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=async%2520getMahasiswa%28%29%257B%250A%2520%2520try%2520%257B%250A%2520%2520%2520%2520const%2520response%2520%253D%2520await%2520fetch%28%27http%253A%252F%252Flocalhost%253A8008%252Fapi%252Fmahasiswa%252F%27%29%250A%2520%2520%2520%2520const%2520data%2520%253D%2520await%2520response.json%28%29%250A%2520%2520%2520%2520console.log%28data%29%250A%2520%2520%2520%2520this.datamahasiswa%2520%253D%2520data.data%250A%2520%2520%257D%2520catch%2520%28error%29%2520%257B%250A%2520%2520%2520%2520console.error%28error%29%250A%2520%2520%257D%250A%257D"
  style="width: 700px; height: 375px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

### POST

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=async%2520addMahasiswa%28mahasiswa%29%2520%257B%250A%2520%2520try%2520%257B%250A%2520%2520%2520%2520const%2520response%2520%253D%2520await%2520fetch%28%27http%253A%252F%252Flocalhost%253A8008%252Fapi%252Fmahasiswa%252F%27%252C%2520%257B%250A%2520%2520%2520%2520%2520%2520method%253A%2520%27POST%27%252C%250A%2520%2520%2520%2520%2520%2520body%253A%2520JSON.stringify%28mahasiswa%29%252C%250A%2520%2520%2520%2520%2520%2520headers%253A%2520%257B%2520%27Content-type%27%253A%2520%27application%252Fjson%253B%2520charset%253DUTF-8%27%2520%257D%252C%250A%2520%2520%2520%2520%257D%29%250A%2520%2520%2520%2520const%2520dataresponse%2520%253D%2520await%2520response.json%28%29%250A%2520%2520%2520%2520this.datamahasiswa%2520%253D%2520%255B...this.datamahasiswa%252C%2520dataresponse.data%255D%250A%2520%2520%257D%2520catch%2520%28error%29%2520%257B%250A%2520%2520%2520%2520console.error%28error%29%250A%2520%2520%257D%250A%257D"
  style="width: 700px; height: 432px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

### PUT

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=async%2520editMahasiswa%28id%252C%2520updatedMahasiswa%29%2520%257B%250A%2520%2520try%2520%257B%250A%2520%2520%2520%2520const%2520response%2520%253D%2520await%2520fetch%28%250A%2520%2520%2520%2520%2520%2520%2560http%253A%252F%252Flocalhost%253A8008%252Fapi%252Fmahasiswa%252F%2524%257Bid%257D%2560%252C%250A%2520%2520%2520%2520%2520%2520%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520method%253A%2520%27PUT%27%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520body%253A%2520JSON.stringify%28updatedMahasiswa%29%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520headers%253A%2520%257B%2520%27Content-type%27%253A%2520%27application%252Fjson%253B%2520charset%253DUTF-8%27%2520%257D%252C%250A%2520%2520%2520%2520%2520%2520%257D%250A%2520%2520%2520%2520%29%253B%250A%2520%2520%2520%2520const%2520dataresponse%2520%253D%2520await%2520response.json%28%29%253B%250A%2520%2520%2520%2520this.datamahasiswa%2520%253D%2520this.datamahasiswa.map%28%28mahasiswa%29%2520%253D%253E%250A%2520%2520%2520%2520%2520%2520mahasiswa.id%2520%253D%253D%253D%2520id%2520%253F%2520dataresponse.data%2520%253A%2520mahasiswa%250A%2520%2520%2520%2520%29%253B%250A%2520%2520%257D%2520catch%2520%28error%29%2520%257B%250A%2520%2520%2520%2520console.error%28error%29%253B%250A%2520%2520%257D%250A%257D"
  style="width: 700px; height: 526px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

### DELETE

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=monokai&wt=none&l=vue&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=false&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=13.5px&lh=140%25&si=false&es=2x&wm=false&code=async%2520deleteEmployee%28id%29%2520%257B%250A%2520%2520try%2520%257B%250A%2520%2520%2520%2520await%2520fetch%28%2560http%253A%252F%252Flocalhost%253A8008%252Fapi%252Fmahasiswa%252F%2524%257Bid%257D%2560%252C%2520%257B%250A%2520%2520%2520%2520%2520%2520method%253A%2520%2522DELETE%2522%250A%2520%2520%2520%2520%257D%29%253B%250A%2520%2520%2520%2520this.datamahasiswa%2520%253D%2520this.datamahasiswa.filter%28mahasiswa%2520%253D%253E%2520mahasiswa.id%2520%21%253D%253D%2520id%29%253B%250A%2520%2520%257D%2520catch%2520%28error%29%2520%257B%250A%2520%2520%2520%2520console.error%28error%29%253B%250A%2520%2520%257D%250A%257D"
  style="width: 700px; height: 375px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Dan aplikasi selesai.




