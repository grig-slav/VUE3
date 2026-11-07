<script setup>
defineProps({
    name:String,
    age:Number
})
</script>
<template>
     <div class="opisan">
            <ul>
                <li>имя:{{ name }}</li>
                <li>возраст:{{ age }}</li>
            </ul>
        </div>
</template>