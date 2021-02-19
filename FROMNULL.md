# Create Basic VUE-APP
Instruksi Project Dari nol

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

  ```bash
    Vue CLI v4.5.11
    ? Please pick a preset:
      Default ([Vue 2] babel, eslint)
      Default (Vue 3 Preview) ([Vue 3] babel, eslint)
    > Manually select features
  ```

	Untuk sementara kita hanya centang `Choose Vue version`
  ```
    Vue CLI v4.5.11
    ? Please pick a preset: Manually select features
    ? Check the features needed for your project:
    >(*) Choose Vue version
    ( ) Babel
    ( ) TypeScript
    ( ) Progressive Web App (PWA) Support
    ( ) Router
    ( ) Vuex
    ( ) CSS Pre-processors
    ( ) Linter / Formatter
    ( ) Unit Testing
    ( ) E2E Testing
  ```

	Disini kita akan menggunakan yang versi 2.x
  ```
    Vue CLI v4.5.11
    ? Please pick a preset: Manually select features
    ? Check the features needed for your project: Choose Vue version
    ? Choose a version of Vue.js that you want to start the project with (Use arrow keys)
    > 2.x
      3.x (Preview)
  ```
	
	Silahkan anda pilih letak config untuk Babel, ESlint, dll berada. Kalau saya lebih suka saya taruh di package.json
  ```
    ? Where do you prefer placing config for Babel, ESLint, etc.?
    In dedicated config files
    > In package.json
  ```
	
	Setelah semua instalasi selesai, kita bisa berpindah ke direktori project yang sudah dibuat dan run project dengan perintah seperti dibawah ini:
	```
    cd vue-app

    npm run serve
    # or
    yarn serve
  ```
	
	Pada titik ini kita sudah selesai mempersiapkan semua yang dibutuhkan untuk membangun Vue aplikasi. jangan lupa tambahkan plugin Vetur untuk formatter dan highlight pada text editor anda dan juga install ekstensi Vue Devtools untuk memberi informasi tentang *components* - *state, method, data,* dll ketika anda *running* vue pada browser anda.


# Getting Started
Selamat kita sudah me-setting Vue boilerplate app. di projek ini terdapat `public` folder yang didalamnya terdapat `index.html`, dan `src` folder dengan `main.js` sebagai titik awal js. Disini juga kita diperkenalkan pula dengan `.vue` file, dengan komponen `HelloWorld.vue` dan `App.vue`.

## Titik Awal
Pada `main.js` disini membawa Vue dan *redering* App ke app div pada `index.html`. File ini tidak butuh diubah.
```javascript
  import Vue from 'vue'
  import App from './App.vue'

  Vue.config.productionTip = false

  new Vue({
    render: function (h) { return h(App) },
  }).$mount('#app')
```

## Anatomi Vue
Ketika kita akan membuat suatu file `.vue`, selalu terdapat 3 tag yang pasti yaitu:
- `<template>`
- `<script>`
- `<style>`

```vue
  <template></template>

  <script>
    export default {
      name: 'nama-komponen',
    }
  </script>

  <style scoped></style>
```

Setiap data logic pada setiap komponen akan berada pada tag `<script>`, seperti kita tahu `<style>` hanya digunakan untuk CSS, kita juga bisa gunakan `scoped` untuk mengaplikasikan style tersebut tidak secara global.

Karena tujuan dari pembelajaran kali ini adalah tentang fungsionalitas, bukan soal *styling*, saya akan menambahkan secara cepat `Skeleton` framework CSS pada `public/index.html` file untuk lebih memudahkan dalam *styling*.

```vue
  <!DOCTYPE html>
  <html lang="">
    <head>
    <!-- .... isi header -->
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/skeleton/2.0.4/skeleton.min.css">
    </head>
    <body>
      <!-- .... isi body -->
    </body>
  </html>
```

Putar musik lo-fi 🎧 dan mulai memasak 👨‍🍳.


# Creating a Component

Buat file dengan nama `MahasiswaTable.vue` du `src/components`. Kita akan membuat tabel dengan beberapa data statik seperti dibawah ini.

```vue
  <template>
    <div id="mhs-table">
      <table class="u-full-width">
          <thead>
              <tr>
              <th>Nama</th>
              <th>No Induk Mahasiswa</th>
              <th>Email</th>
              </tr>
          </thead>
          <tbody>
              <tr>
              <td>Jonatan Teofilus</td>
              <td>6876879890</td>
              <td>jonatan.teofilus@gmail.com</td>
              </tr>
              <tr>
              <td>Dwayne Johnson</td>
              <td>0978769767</td>
              <td>dwayne150@gmail.com</td>
              </tr>
          </tbody>
      </table>
    </div>
  </template>

  <script>
    export default {
      name: 'mahasiswa-table',
    }
  </script>

  <style scoped>

  </style>
```

Di Vue, import nama file akan menjadi PascalCase, seperti `MahasiswaTable` tapi ketika komponen tersebut digunakan pada `<template>`, akan berubah menjadi kebab-case, `<mahasiswa-table>`. Hal ini supaya kita bisa mengenali konvensi untuk masing-masing javascript dan HTML.

Kita export `mahasiswaTable` dan import ke `App.vue`. Pada waktu me-import, kita bisa menggunakan `@` sebagai referensi `src` folder. App.vue mengenali dan komponen tersebut bisa digunakan melalui `components` property. Jadi semua komponen yang dibutuhkan dalam satu `.vue` harus ditambahkan disana.

```vue
  <template>
    <div id="app">
      <div class="container">
        <h1>Mahasiswa</h1>
        <mahasiswa-table/>
      </div>
    </div>
  </template>

  <script>
  import MahasiswaTable from '@/components/MahasiswaTable.vue'
  export default {
    name: 'App',
    components: {
      MahasiswaTable
    }
  }
  </script>

  <style scoped>
  </style>
```

Akan tampil seperti ini:
####gambar review

Supaya data pada tabel menjadi dinamis, kita akan ubah menjadi array object. Jadi mari kita tambah method `data()` dan return array mahasiswa. kita juga menambahkan ID untuk setiap item agar membuatnya untuk dan teridentifikasi.

Sekarang kita memiliki data tersebut pada `App.vue`, tapi kita harus bawa data tersebut ke `MahasiswaTable`. Kita bisa melakukan hal itu dengan *passing* date sebagai properti. Sebuah atribut dengan *colon* `:` untuk mengirim data pada. `:` juga merupakan *shorthand* dari `v-bind`. Dalam kasus ini kita akan membawa array datamahasiswa.

```vue
  <mahasiswa-table :datamahasiswa="datamahasiswa"/>
  <!-- atau -->
  <mahasiswa-table v-bind:datamahasiswa="datamahasiswa"/>
```

Saat ini pada sisi `MahasiswaTable`, kita ingin mengambil data tersebut, jadi kita harus membuat `props` attribute dengan nama `datamahasiswa`.

## Loops

Sekarang kita telah mendapatkan data tersebut, kita butuh mengulang data dan menampilkanya ke DOM. Kita bisa lakukan ini dengan menggunakan `v-for` attribute. Sekarang kita telah mendapatkan `datamahasiswa` di `MahasiswaTable` kita tampilkan per baris.

```vue
  <template>
    <div id="mhs-table">
      <table class="u-full-width">
          <thead>
              <tr>
              <th>Nama</th>
              <th>No Induk Mahasiswa</th>
              <th>Email</th>
              </tr>
          </thead>
          <tbody>
              <tr v-for="mahasiswa in datamahasiswa" :key="mahasiswa.id">
                  <td>{{ mahasiswa.nama }}</td>
                  <td>{{ mahasiswa.npm }}</td>
                  <td>{{ mahasiswa.email }}</td>
              </tr>
          </tbody>
      </table>
    </div>
  </template>
```



# Form

Kita sekarang membuat form tambah mahasiswa. 

Buat `MahasiswaForm.vue` dan atur field nama, npm, email dan juga `button` submit. Juga buat data object mahasiswa dengan nama, npm dan juga email.

```vue
  <template>
    <form>
      <div class="row">
          <label for="inputNama">Nama Mahasiswa</label>
          <input class="u-full-width" type="text" placeholder="Nama Mahasisiwa" id="inputNama">
          <label for="inputNpm">Nomer Induk Mahasiswa</label>
          <input class="u-full-width" type="text" placeholder="Nomor Induk Mahasiswa" id="inputNpm">
          <label for="inputNama">Email Mahasiswa</label>
          <input class="u-full-width" type="email" placeholder="Email Mahasisiwa" id="inputEmail">
          <button class="button-primary">Add Mahasiswa</button>
      </div>
    </form>
  </template>

  <script>
  export default {
      data() {
          return {
              mahasiswa:{
                  nama:'',
                  npm:'',
                  email:''
              }
          }
      },
  }
  </script>

  <style scoped>
    form {
      margin-bottom: 2rem;
    }
  </style>
```


Kita juga menambahkan beberapa baris code pada `App.vue`

```vue
  <template>
    <div id="app">
      <div class="container">
        <h1>Mahasiswa</h1>
        <mahasiswa-form/>
        <mahasiswa-table :datamahasiswa="datamahasiswa"/>
      </div>
    </div>
  </template>

  <script>
  import MahasiswaTable from '@/components/MahasiswaTable.vue'
  import MahasiswaForm from '@/components/mahasiswaForm.vue'
  export default {
    name: 'App',
    components: {
      MahasiswaTable,
      MahasiswaForm
    },
    data() {
      //...
    },
  }
  </script>

  <style scoped>
  </style>
```

Sekarang gimana caranya mendapatkan data dan mengirimkannya ke Vue component state. Untuk itu kita gunakan `v-model`. `v-model` suatu *sytactic sugar* built-in Vue untuk mengubah input value ketika ada event `onchange`.

```vue
<template>
  <form>
    <div class="row">
        <label for="inputNama">Nama Mahasiswa</label>
        <input v-model="mahasiswa.nama" class="u-full-width" type="text" placeholder="Nama Mahasisiwa" id="inputNama">
        <label for="inputNpm">Nomer Induk Mahasiswa</label>
        <input v-model="mahasiswa.npm" class="u-full-width" type="text" placeholder="Nomor Induk Mahasiswa" id="inputNpm">
        <label for="inputNama">Email Mahasiswa</label>
        <input v-model="mahasiswa.email" class="u-full-width" type="email" placeholder="Email Mahasisiwa" id="inputEmail">
        <button class="button-primary">Add Mahasiswa</button>
    </div>
  </form>
</template>
```

Sekarang kita bisa tambahkan ini, kita bisa lihati di Vue DevTools ketika *state* pada komponen berubah. 
Kita tinggal submit lalu update ke parent `(App)` state dengan object mahasiswa baru.


# Event listeners

Untuk submit form kita tambahkan atribut `v-on:submit` atau kita bisa gunakan `@submit` untuk shorthand pada tag `<form>`. ini sama dengan event `@click/v-on:click`. Event submit juga memiliki `prevent` yang difungsikan untuk mematikan method GET/POST yang secara default sudah disediakan oleh form.

Mari kita tambah script ini ke form, dan juga buat method submitMahasiswa.

```vue
<form @submit.prevent="submitMahasiswa"></form>
```

# Methods

Saat ini kita membuat method pertama pada component. Dibawah `data()`, kita bisa buat object `methods`, dimana akan menampung semua custom method yang kita buat. mari kita buat `submitMahasiswa` disana.

```vue
<script>
export default {
    data() {
        return {
            mahasiswa:{
                nama:'',
                npm:'',
                email:''
            }
        }
    },
    methods: {
      submitMahasiswa() {
        console.log("test submited")
      }
    },
}
</script>
```

# Emitting events

Sekarang kita coba submit form, kita akan melihat message log di console, lalubagaimana caranya kita mengirimkan data ke parent `App` sekarang? tentunya kita bisa melakukan hal tersebut dengan `$emit`

Emit mengirim nama event dan data ke parent component, seperti ini:

```javascript
this.$emit('nama-emit-event', dataPass)
```


pada case kita, kita akan buat event dengan nama `add:mahasiswa` dan membawa data `this.mahasiswa`

```javascript
submitMahasiswa() {
        this.$emit("add:mahasiswa",this.mahasiswa)
}
```

Ketika sudah ditambahakan, klik untuk add form lalu ke Vue DevTools. kita akan lihat notifikasi untuk event baru, dan akan memberi tahu kuta tentang nama, source, dan payload, dimana pada kasus ini object terbuat.

## Menerima Event dari child component

hal pertama yang harus dilakukan adalah membuat supaya `mahasiswa-form` untuk me-handle event yang di-emmit untuk memanggil ke method baru. contoh seperti ini:

```vue
<component @name-of-emitted-event="methodToCallOnceEmitted"></component>
```

Mari kita tambah ke App.vue.

```vue
<mahasiswa-form @add:mahasiswa="addMahasiswa"/>
```

Kita hanya perlu membuat method `addMahasiswa` di `App.vue`, dimana memodifikasi array `datamahasiswa` dengan menambah item baru kedalamnya.
kode dibawah adalah untuk mendapatkan `id` mahasiswa baru berdasarkan nomer item array. Pada database sebenarnya, `id` sudah tergenerate secara unik atau *auto increment*.

```javascript
addMahasiswa(mahasiswa) {

  const lastId = this.datamahasiswa.length > 0? this.datamahasiswa[this.datamahasiswa.length - 1].id: 0 ;
  const id = lastId + 1;
  // Using spread untuk will clone your object.
  const newMahasiswa = { ...mahasiswa, id };
  // spread untuk mengulang
  this.datamahasiswa = [...this.datamahasiswa, newMahasiswa];
}
```


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

```javascript
computed: {
  invalidNama() {
    return this.mahasiswa.nama === ''
  },
  invalidNpm() {
    return this.mahasiswa.npm === ''
  },
  invalidEmail() {
    return this.mahasiswa.email === ''
  },
},
```

Kita juga membutuhkan `submitting` *state* untuk mengecek apakah form sudah tersubmit, `error` *state*  jika sesuatu salah dan `success` *state* jika form input benar.

```javascript
data() {
    return {
      submitting: false,
      error: false,
      success: false,
      mahasiswa:{
          nama:'',
          npm:'',
          email:''
      }
    }
},
```

Fungsi submit pertama akan mereset ulang state baik itu succes atau error yang telah terseting, mulai submit, setelah itu cek semua method `computed` dan jika terdapat return *true*, maka error state akan diset. Jika tida kita bisa submit, dan mengatur state sukses dan semua state kembali seperti semula.

```javascript
methods: {
  submitMahasiswa() {
    // set state menjadi tersubmit
    this.submitting = true
    // bersihkan terlebih dahulu state error & success
    this.clearStatus()

    // panggil setiap computed fungsi untuk validasi
    if (this.invalidNama || this.invalidNpm || this.invalidEmail) {
      this.error = true
      return
    }

    // emit ke parent
    this.$emit("add:mahasiswa",this.mahasiswa)

    // kosongkan kembali obj mahasiswa
    this.clearMahasiswa()

    // set sukses
    this.error = false
    this.success = true
    // set status submit jadi false
    this.submitting = false
  },
  clearStatus() {
    this.success = false
    this.error = false
  },
  clearMahasiswa(){
    this.mahasiswa = {
      nama:'',
      npm:'',
      email:''
    }
  }
},
```

Saya juga tambahkan bebarapa baris CSS untuk kondisi success state dan error state.

```css
<style scoped>
  form {
    margin-bottom: 2rem;
  }
  
  [class*='-message'] {
    font-weight: 500;
  }

  .error-message {
    color: #d33c40;
  }

  .success-message {
    color: #32a95d;
  }

  input.has-error {
    border: 1.5px solid #d33c40;;
  }
</style>
```

Akhirnya kita telah mengatur form. Jika form tersubmit dan satu dari antara computed preoperty tidak valid, kita akan set class `has-error` pada input. Gunakan `:class=` untuk memastikan bahwa class akan diterapkan melalui Javascript. Kita juga pastikan pesan success dan error tertampil di atas form.

```vue
<form @submit.prevent="submitMahasiswa">
  <div class="row">
      <label for="inputNama">Nama Mahasiswa</label>
      <input v-model="mahasiswa.nama" class="u-full-width" :class="{ 'has-error': submitting && invalidNama }" type="text" placeholder="Nama Mahasisiwa" id="inputNama">

      <label for="inputNpm">Nomer Induk Mahasiswa</label>
      <input v-model="mahasiswa.npm" class="u-full-width" :class="{ 'has-error': submitting && invalidNpm }" type="text" placeholder="Nomor Induk Mahasiswa" id="inputNpm">

      <label for="inputNama">Email Mahasiswa</label>
      <input v-model="mahasiswa.email" class="u-full-width" :class="{ 'has-error': submitting && invalidEmail }" type="email" placeholder="Email Mahasisiwa" id="inputEmail">

      <p v-if="error && submitting" class="error-message">
        ❗Isi file yang dibutuhkan
      </p>
      <p v-if="success" class="success-message">✅ Sukses menambahkan mahasiswa.</p>

      <button class="button-primary">Add Mahasiswa</button>
  </div>
</form>
```


# Delete

Form sudah selesai, sekarang tinggal update dan delete. Hal pertama yang akan kita kerjakan yaitu menambahkan baris `aksi`, dan button untuk edit dan delete.

```vue
<template>
  <div id="mhs-table">
    <table class="u-full-width">
        <thead>
            <tr>
            <th>Nama</th>
            <th>No Induk Mahasiswa</th>
            <th>Email</th>
            <th>Aksi</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="mahasiswa in datamahasiswa" :key="mahasiswa.id">
                <td>{{ mahasiswa.nama }}</td>
                <td>{{ mahasiswa.npm }}</td>
                <td>{{ mahasiswa.email }}</td>
                <td>
                    <button>edit</button>
                    <button>delete</button>
                </td>
            </tr>
        </tbody>
    </table>
  </div>
</template>

<script>
export default {
    props:["datamahasiswa"],
}
</script>

<style scoped>
    button {
        margin:2px
    }
</style>
```

kita akan emit dan membawa id untuk memanggil fungsi `deleteMahasiswa` yang nanti akan kita buat pada parent.

```vue
<button @click="$emit('delete:mahasiswa', mahasiswa.id)">Delete</button>
```

kembali ke `App.vue`, kita telah menambah event aksi on delete-mahasiswa pada `mahasiswa-table`, tambahakan fungsi untuk menghandler event tersebut.

```vue
<mahasiswa-table @delete:mahasiswa="deleteMahasiswa" :datamahasiswa="datamahasiswa"/>
```

dan kita lakukan filter array dengan menambahkan method `deleteMahasiswa` dan dengan logika seperti dibawah.

```javascript
deleteMahasiswa(id){
  this.datamahasiswa = this.datamahasiswa.filter(mahasiswa => mahasiswa.id !== id)
}
```

Sekarang kita bisa hapus item. mari kita buat pesan untuk memberi info data mahasiswa kosong jika array `datamahasiswa` kosong.

```vue
<div id="mhs-table">
    <p v-if="datamahasiswa < 1"> data mahasiswa kosong</p>
    <table v-else class="u-full-width">
		...
    </table>
</div>
```

Kita telah selesai menghapus item mahasiswa.


# Edit item

Editing is a little more complex than deleting. The setup from App.vue is simple though, so we'll do that first. Just add the edit:employee event that we'll be making:

Edit data seding lebih *tricky* dibandingkan dengan delete. Hal pertama yang dilakukan yaitu kita tambah event `edit:mahasiswa` dan kita juga buatkan method untuk menghadle event tersebut dengan nama `editMahasiswa` sama seperti delete.

```vue
<mahasiswa-table 
  @delete:mahasiswa="deleteMahasiswa" 
  @edit:mahasiswa="editMahasiswa"
  :datamahasiswa="datamahasiswa"/>
```

dan pada method `editMahasiswa`, kita akan ambil data dari array berdasarkan id lalu kita update.

```javascript
editMahasiswa(id, updatemahasiswa){
      this.datamahasiswa = this.datamahasiswa.map(mahasiswa => mahasiswa.id == id ? updatemahasiswa : mahasiswa);
}
```

Cukup mudah.

Sekarang kembali ke `MahasiswaTable.vue`, kita ingin buat "edit mode" enable ketika button terklik.

```vue
<button @click="editMode(mahasiswa.id)">Edit</button>
```

kita akan membuat editing state dan akan get dan set id pada row yang sedang pada posisi edited ketika `editMode` enabled. `MahasiswaTable` memiliki local method `editMahasiswa` yang memiliki fungsi untuk emit `edit:mahasiswa` di App jika semua value field tidak kosong, proses kedua yaitu kita reset edit state.

```javascript
data() {
    return {
        editing: null,
    }
},
methods: {
    editMode(id) {
        this.editing = id
    },
    editMahasiswa(mahasiswa) {
        if (mahasiswa.nama === '' || mahasiswa.email === '' || mahasiswa.npm === '') return
        this.$emit('edit:mahasiswa', mahasiswa.id, mahasiswa)
        this.editing = null
    }
}
```

untuk membuat editable, kita akan cek data `editing === mahasiswa.id` kalau sama pada baris tersebut, maka input akan ditampilkan. kita juga tambahkan button `cancel` untuk mebatalkan edit dan set `editing` menjadi null.

```vue
<tr v-for="mahasiswa in datamahasiswa" :key="mahasiswa.id">
    <td v-if="editing === mahasiswa.id">
        <input type="text" v-model="mahasiswa.nama" placeholder="Nama Mahasiswa"/>
    </td>
    <td v-else>{{ mahasiswa.nama }}</td>
    <td v-if="editing === mahasiswa.id">
        <input type="text" v-model="mahasiswa.npm" placeholder="Nomor Induk Mahasiswa"/>
    </td>
    <td v-else>{{ mahasiswa.npm }}</td>
    <td v-if="editing === mahasiswa.id">
        <input type="email" v-model="mahasiswa.email" placeholder="Email Mahasiswa"/>
    </td>
    <td v-else>{{ mahasiswa.email }}</td>
    <td v-if="editing === mahasiswa.id">
        <button class="button-primary" @click="editMahasiswa(mahasiswa)">Save</button>
        <button @click="editing = null">Cancel</button>
    </td>
    <td v-else>
        <button @click="editMode(mahasiswa.id)">Edit</button>
        <button @click="$emit('delete:mahasiswa',mahasiswa.id)">delete</button>
    </td>
</tr>
```

edit telah berhasil, tetapi masih ada masalah yaitu ketika `cancel` data tidak kembali seperti sebelum teredit. Maka dari itu kita butuh caching data mahasiswa sebelu diedit.

```javascript
editMode(mahasiswa) {
    this.cachemahasiswa = {...mahasiswa}
    this.editing = mahasiswa.id
},
cancelEdit(mahasiswa){
    Object.assign(mahasiswa, this.cachemahasiswa)
    this.editing = null
}
```

saat ini kita telah selesai CRUD data mock, namun ketika dir real produksi app akan membuat API call ke back end database. kita akan coba buat.



# Asynchronous REST API

kita akan mengubah data mock dengan real API dan kita akan buat POST, PUT, dan DELETE request. Disini sudah tersedia APInya kita tinggal panggil.

Method asynchronous dengan `async/await` dan menggunakan `try/catch` blok seperti contoh dibawah ini.

sebenarnya untuk `Fetch API` sendiri sudah banyak opsi library node yang terkenal dan bisa digunakan seperti `Axios` dll. Namun disini saya hanya menggunakan `Fetch`, fetch merupakan bawaan dari javascript untuk async fetch API dan alasan lain yaitu karena tidak perlu menginstall depedensi dan tujuan sampel.

```javascript
async asynchronousMethod() {
  try {
    const response = await fetch('url')
    const data = await response.json()

    // do something with `data`
  } catch (error) {
    // do something with `error`
  }
}
```

## Lifecycle methods

Ketika GET request, kita akan menghapus semua data array mahasiswa yang kita punya, lalu mengganti data tersebut dengan get dari API. Kita panggil GET pada saat vue `mounted` lifecycle method.

kenapa pada saat `mounted`?. Mounted dijalankan ketika component semua sudah terisi ke DOM. ini adalah cara yang biasa dilakukan ketika ingin menampilkan data dari API.

```javascript
export default {
  name: 'App',
  components: {
    MahasiswaTable,
    MahasiswaForm
  },
  data() {
	...
  },
  mounted() {
    this.getMahasiswa()
  },
  methods: {
	...
  }
}
```

### GET
Mengambil data.

```javascript
async getMahasiswa(){
  try {
    const response = await fetch('http://localhost:8008/api/mahasiswa/')
    const data = await response.json()
    console.log(data)
    this.datamahasiswa = data.data
  } catch (error) {
    console.error(error)
  }
}
```

### POST

```javascript
async addMahasiswa(mahasiswa) {
  try {
    const response = await fetch('http://localhost:8008/api/mahasiswa/', {
      method: 'POST',
      body: JSON.stringify(mahasiswa),
      headers: { 'Content-type': 'application/json; charset=UTF-8' },
    })
    const dataresponse = await response.json()
    this.datamahasiswa = [...this.datamahasiswa, dataresponse.data]
  } catch (error) {
    console.error(error)
  }
}
```

### PUT

```javascript
async editMahasiswa(id, updatedMahasiswa) {
  try {
    const response = await fetch(
      `http://localhost:8008/api/mahasiswa/${id}`,
      {
        method: 'PUT',
        body: JSON.stringify(updatedMahasiswa),
        headers: { 'Content-type': 'application/json; charset=UTF-8' },
      }
    );
    const dataresponse = await response.json();
    this.datamahasiswa = this.datamahasiswa.map((mahasiswa) =>
      mahasiswa.id === id ? dataresponse.data : mahasiswa
    );
  } catch (error) {
    console.error(error);
  }
}
```

### DELETE

```javascript
async deleteEmployee(id) {
  try {
    await fetch(`http://localhost:8008/api/mahasiswa/${id}`, {
      method: "DELETE"
    });
    this.datamahasiswa = this.datamahasiswa.filter(mahasiswa => mahasiswa.id !== id);
  } catch (error) {
    console.error(error);
  }
}
```

Dan violaa ✨✨ aplikasi selesai.




