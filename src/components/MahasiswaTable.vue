<template>
  <div id="mhs-table">
    <p v-if="datamahasiswa < 1"> data mahasiswa kosong</p>
    <table v-else class="u-full-width">
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
                    <button @click="cancelEdit(mahasiswa)">Cancel</button>
                </td>
                <td v-else>
                    <button @click="editMode(mahasiswa)">Edit</button>
                    <button @click="$emit('delete:mahasiswa',mahasiswa.id)">delete</button>
                </td>
            </tr>
        </tbody>
    </table>
  </div>
</template>

<script>
export default {
    props:["datamahasiswa"],
    data() {
        return {
            editing: null,
        }
    },
    methods: {
        editMode(mahasiswa) {
            this.cachemahasiswa = {...mahasiswa}
            this.editing = mahasiswa.id
        },
        cancelEdit(mahasiswa){
            Object.assign(mahasiswa, this.cachemahasiswa)
            this.editing = null
        },
        editMahasiswa(mahasiswa) {
            if (mahasiswa.nama === '' || mahasiswa.email === '' || mahasiswa.npm === '') return
            this.$emit('edit:mahasiswa', mahasiswa.id, mahasiswa)
            this.editing = null
        }
    }
}
</script>

<style scoped>
    button {
        margin:2px
    }
</style>