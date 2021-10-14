<template>
    <div id="app">
        What I Do Today
    </div>
    <div class="pekerjaan-rumah">
        <div v-for="tugasSaya in tugas" v-bind:key="tugasSaya.id" class="tugas">
         
          <div class="form-check">
  <input class="form-check-input" type="checkbox" value="" id="flexCheckDefault">
  <label class="form-check-label" for="flexCheckDefault">
    {{tugasSaya.nama}}
  </label>
</div>
        </div>     
    </div>
</template>

<script>

export default {
  name: 'App',
  data:function() {
    return( {
    tugas: [
      {
      id:1,
      nama: "Membersihkan Toilet",
      isDone: false
    },
      {
      id:2,
      nama: "Membersihkan Kasur",
      isDone: false
    },
      {
      id:3,
      nama: "Membersihkan SpringBed",
      isDone: false
    },
    ]
  });
  }
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
