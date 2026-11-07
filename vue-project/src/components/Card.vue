<script setup>
import { ref } from 'vue';
// defineProps({
//     name:String,
//     age:Number
// })  
const props=defineProps({
    name:String,
    age:Number,
    id:Number
})
const emit=defineEmits([
    'delete-user'
])
function deleteUser(){
    emit('delete-user',props.id)

}


</script>

<template>
    <div class="all">
        <h1 class="zag">Карточка Ученика</h1>
    <div class="osn">
        <h3 class="zag">ЛУЧШИЙ УЧЕНИК</h3>
        <div class="image">ФОТО</div>
        <div class="opisan">
            <ul>
                <li>имя:{{ name }}</li>
                <li>возраст:{{ age }}</li>
                
            </ul>
        </div>
        <button @click="deleteUser">delete</button>
    </div>
    </div>
</template>

<style scoped>
.all{
    display: flex;
    justify-content: center;
    text-align: center;
    align-items: center;
    flex-direction: column;
}
.osn{
    padding: 30px   ;
    border: 1px solid black;
    border-radius: 20px;
    background-color: bisque;
    margin: 10px;   
}
.opisan{
    display: flex;
    justify-content: flex-start;
    text-align: left;
}
.image{
    border:1px solid black;
}
</style>
