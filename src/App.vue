<template>
  <div id="app">
    <div class="container">
      <h1>Mahasiswa</h1>
      <mahasiswa-form @add:mahasiswa="addMahasiswa" />
      <mahasiswa-table
        @delete:mahasiswa="deleteMahasiswa"
        @edit:mahasiswa="editMahasiswa"
        :datamahasiswa="datamahasiswa"
      />
      <!-- atau -->
      <!-- <mahasiswa-table v-bind:datamahasiswa="datamahasiswa"/> -->
    </div>
  </div>
</template>

<script>
import MahasiswaTable from '@/components/MahasiswaTable.vue';
import MahasiswaForm from '@/components/MahasiswaForm.vue';
export default {
  name: 'App',
  components: {
    MahasiswaTable,
    MahasiswaForm,
  },
  data() {
    return {
      datamahasiswa: [
        {
          id: 1,
          nama: 'Jonatan Teofilus',
          npm: '6876879890',
          email: 'jonatan.teofilus@gmail.com',
        },
        {
          id: 2,
          nama: 'Dwayne Johnson',
          npm: '0978769767',
          email: 'dwayne150@gmail.com',
        },
      ],
    };
  },
  mounted() {
    // console.log('fungsi ini dipanggil ketika, mounted')
    this.getMahasiswa();
  },
  methods: {
    async getMahasiswa() {
      try {
        const response = await fetch('http://localhost:8008/api/mahasiswa/');
        const dataresponse = await response.json();
        this.datamahasiswa = dataresponse.data;
      } catch (error) {
        console.error(error);
      }
    },
    async addMahasiswa(mahasiswa) {
      try {
        const response = await fetch('http://localhost:8008/api/mahasiswa/', {
          method: 'POST',
          body: JSON.stringify(mahasiswa),
          headers: { 'Content-type': 'application/json; charset=UTF-8' },
        });
        const dataresponse = await response.json();
        this.datamahasiswa = [...this.datamahasiswa, dataresponse.data];
      } catch (error) {
        console.error(error);
      }
    },
    async deleteMahasiswa(id) {
      try {
        await fetch(`http://localhost:8008/api/mahasiswa/${id}`, {
          method: "DELETE"
        });
        this.datamahasiswa = this.datamahasiswa.filter(mahasiswa => mahasiswa.id !== id);
      } catch (error) {
        console.error(error);
      }
    },
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
    },
  },
};
</script>

<style scoped></style>
