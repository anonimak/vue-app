<template>
  <form @submit.prevent="submitMahasiswa">
    <div class="row">
              
        <p v-if="error && submitting" class="error-message">
          Isi file yang dibutuhkan
        </p>
        <p v-if="success" class="success-message">Sukses menambahkan mahasiswa.</p>


        <label for="inputNama">Nama Mahasiswa</label>
        <input v-model="mahasiswa.nama" class="u-full-width" :class="{ 'has-error': submitting && invalidNama }" type="text" placeholder="Nama Mahasisiwa" id="inputNama">
        
        <label for="inputNpm">Nomer Induk Mahasiswa</label>
        <input v-model="mahasiswa.npm" class="u-full-width" :class="{ 'has-error': submitting && invalidNpm }" type="text" placeholder="Nomor Induk Mahasiswa" id="inputNpm">
        
        <label for="inputNama">Email Mahasiswa</label>
        <input v-model="mahasiswa.email" class="u-full-width" :class="{ 'has-error': submitting && invalidEmail }" type="email" placeholder="Email Mahasisiwa" id="inputEmail">
        
        <button class="button-primary">Add Mahasiswa</button>
    </div>
  </form>
</template>

<script>
export default {
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
}
</script>

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