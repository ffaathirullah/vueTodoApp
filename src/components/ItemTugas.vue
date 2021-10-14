<template>
    <div>
    <input class="form-check-input" onClick="" type="checkbox" value="" id="flexCheckDefault">
     <label class="form-check-label item" v-bind:class="{ 'item-completed': tugasSaya.isDone }" for="flexCheckDefault">
       {{tugasSaya.nama}}
    </label>
    </div>
</template>

<script>
export default {
    name: 'ItemTugas',
    props: ["tugasSaya"]
}
</script>

<style scoped>

</style>