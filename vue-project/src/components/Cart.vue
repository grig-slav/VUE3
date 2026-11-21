<script setup lang="ts">
import { ref } from 'vue';
const props=defineProps<{
  id:number
  name:string
  age:number
}>()
const emit=defineEmits<{
  deleteUser:[id:number]
}>()
function removeId(){
  emit('deleteUser',props.id)
}

</script>
<template>
    <div class="cart">
        <h2>{{ name }}</h2>
        <p>Возраст:{{ age }}</p>
        <button @click="removeId">Удалить</button>
    </div>
</template>
<style scoped>
.cart{
    border: 1px solid black;
    border-radius: 10px;
    padding: 20px;
}
</style>