<template>
  <div class="student-card">
    <h1>Карточка студента</h1>
    
    <div class="info-group">
      <p><strong>Имя:</strong> {{ name }}</p>
      <p><strong>Возраст:</strong> {{ age }} лет</p>
      <p><strong>Город:</strong> {{ city }}</p>
      <p><strong>Направление обучения:</strong> {{ fieldOfStudy }}</p>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const name = ref('Григорьев ВячесЛав')
const age = ref(15)
const city = ref('Краснодар')
const fieldOfStudy = ref('WEB-разработка')
</script>

<style scoped>
.student-card {
  max-width: 400px;
  margin: 50px auto;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  background-color: #f9f9f9;
  font-family: Arial, sans-serif;
  color: #333;
}

h1 {
  color: #42b883; 
  text-align: center;
  margin-bottom: 20px;
}

.info-group p {
  font-size: 16px;
  line-height: 1.6;
  margin: 10px 0;
  border-bottom: 1px solid #eee;
  padding-bottom: 5px;
}

strong {
  color: #2c3e50;
}
</style>
