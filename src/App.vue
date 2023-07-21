<script setup>
import {ref} from 'vue'
let msg = "Hallo Dunia";
let pesan3 = ref("Hai!")
let headName = "<h1> nama saya Athhar</h1>";
let pesan1 = "Anda membuat halaman ini pada jam " + new Date().toLocaleString();
let terlihat = true;
let todos = [{ teks: "belajar JavaScript" }, { teks: "Belajar Vue" }, { teks: "Buat proyek keren" }];
let pesan2 = ref("hai vue.js!");
function balikkanPesan() {
  pesan2.value = pesan2.value.split('').reverse('').join('')
}
</script>


<template>
  <div>
    <!-- message -->
    <span>{{ msg }}</span
    ><br />
      <!-- color -->
    <span style="color: red">ini warna merah</span>
    <br />
    <!-- memakai sintaks html -->
    <span v-html="headName"></span>
      <!-- title -->
    <span :title="pesan1"> arahkan cursor kesini </span>
    <br />
      <!-- if -->
    <span v-if="terlihat">saya bisa dilihat</span>
    <br>
      <!-- for -->
    <ol>
      <li v-for="todo in todos">
        {{ todo.teks }}
      </li>
    </ol>
    <br />
    <!-- split button -->
    <p>{{ pesan2 }}</p>
    <button v-on:click="balikkanPesan">Balikkan pesan</button>
    <br>
    <!-- input -->
    <p>{{ pesan3 }}</p>
    <input v-model="pesan3">
  </div>
    
</template>
