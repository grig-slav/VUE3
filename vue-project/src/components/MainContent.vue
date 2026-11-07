<script setup>
import{ref} from 'vue'
import UserInfo from './UserInfo.vue';
import Card from './Card.vue';
const users=ref([
    {
        id:1,
        name:"LEW",
        age:20,
        active:true
    },
    {
        id:2,
        name:'lleeeV',
        age:111,
        active:true
    },
    {
        id:3,
        name:'LLLLeeeV',
        age:1,
        active:false
    }
])
const props=defineProps({
    name:String,
    age:Number
})
function showUser(){
    console.log(props.name)
    console.log(props.age)

}
const count=ref(0)
</script>
<template>
    <div class="cont">
        <h1>Описание страницы</h1>
        <li>Почему мы так часто откладываем важные разговоры? Страх услышать «нет», </li>
            <li>боязнь показаться навязчивыми или просто привычка прятаться за делами — у каждого своя причина. </li>
            <li>Но именно в этих разговорах рождается настоящая близость. </li>
           <li> Попробуйте сегодня сказать кому-то что-то важное — пусть даже простое «спасибо» или «я тебя ценю». Иногда этого достаточно,</li>
             <li>чтобы день стал светлее.</li>

    </div>
    <Card  v-for="user in users":key="user.id"
    :name="user.name"
    :age="user.age"
    :active="user.active"/>
    <UserInfo
    name="Lev"
    :age="40"/>
    <UserInfo
    name="Lev1"
    :age="41"/>
    <UserInfo
    name="Lev2"
    :age="42"/>
    <button @click="showUser">SHOW</button>
</template>
<style scoped>
.cont{
    display:flex;
    justify-content: center;
    align-items:center ;
    flex-direction: column;
}
</style>