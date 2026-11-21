<script setup>
const users=[
    {
        id:1,
        name:"zxc",
        age:20
    },
    {
        id:2,
        name:"asd",
        age:22
    },
    {
        id:3,
        name:"qwe",
        age:25
    }
]
</script>
<template>
    <div v-for="user in users":key=user.id>
        <slot :user="user"></slot>                  
        <!--!!!!!!!!!!!!!!!!!!!!!!!! ПАРАМЕТР СЛОТА, ОГРАНИЧЕННАЯ ВИДИМОСТЬ СЛОТОВ -->

    </div>
</template>