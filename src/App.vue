<template>
    <div id="app">
        What I Do Today
    </div>
    <div class="pekerjaan-rumah">
        <div v-for="tugasSaya in tugas" v-bind:key="tugasSaya.id" class="tugas">
         
          <div class="form-check">
              <ItemTugas v-bind:tugasSaya="tugasSaya"/>
          </div>
        </div>     
    </div>
</template>

<script>
import ItemTugas from "./components/ItemTugas";
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
      isDone: true
    },
      {
      id:3,
      nama: "Membersihkan SpringBed",
      isDone: false
    },
    ]
  });
  },
  components: {
      ItemTugas
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
.item-completed{
  color: #1abc1a;
}
</style>
