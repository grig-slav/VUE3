<!-- <template>
  <div class="student">
    <h1>Карточка студента</h1>
    
    <div class="info">
      <p><strong>Имя:</strong> {{ name }}</p>
      <p><strong>Возраст:</strong> {{ age }} лет</p>
      <p><strong>Город:</strong> {{ city }}</p>
      <p><strong>Направление обучения:</strong> {{napr}}</p>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const name = ref('Григорьев ВячесЛав')
const age = ref(15)
const city = ref('Краснодар')
const napr = ref('WEB-разработка')
</script>

<style scoped>
.student {
  max-width: 400px;
  margin: 50px auto;
  padding: 20px;
  border-radius: 8px;
  background-color: #ffffff;
  
  color: #333;
}

h1 {
  color: #42b883; 
  text-align: center;
  margin-bottom: 20px;
}

.info p {
  font-size: 16px;
  border-bottom: 1px solid #eee;
}

strong {
  color: #2c3e50;
}
</style> -->



<!-- <script setup>
  import{ref,reactive, computed} from 'vue'
import { renderToWebStream } from 'vue/server-renderer';


  const tasks=ref([
    {id:1,text:"Не получить бан",done:false},
    {id:2,text:"Получить бан",done:false},
    {id:3,text:"Сделать ДЗ",done:false},
    {id:4,text:"Посмотреть расписнаие",done:true},
    {id:5,text:"Собрать уроки",done:true},
  ])

const newTask=ref('')
function addTask(){
  if(newTask.value.trim()==='')return
  tasks.value.push({
    id:Date.now(),
    text:newTask.value,
    done:false,
  })
  newTask.value=''
}

function removeTask(task){
  tasks.value = tasks.value.filter(t => t.id !== task.id)
}


</script>
 

<template>
  <div>
    <h1>Задачи на день</h1>
    <input v-model="newTask" placeholder="Новое задание" @keyup.enter="addTask" />
    <button @click="addTask">Добавить</button>
    <ul>
      <li v-for="task in tasks" :key="task.id">
        <span :style="{textDecoration:task.done?'line-through':'none'}">{{ task.text }}</span>-{{ task.done?"✔":"X" }}
        <button @click="removeTask(task)">Удалить</button>
        <input v-model="task.done" type="checkbox" />


      </li>
    </ul>
  </div>
</template> -->


<!-- <script setup>
  import{ref,reactive, computed} from 'vue'
import { renderToWebStream } from 'vue/server-renderer';


  const tasks=ref([
    {id:1,text:"CS2"},
    {id:2,text:"CS2"},
    {id:3,text:"CS2"},
  ])
const filter=ref('all')//"all"|"active"|"done"
const newTask=ref('')
const visibleTasks=computed(()=>{
  if(filter.value==='active')return tasks.value.filter(t=>!t.done)
  if(filter.value==='done')return tasks.value.filter(t=>t.done)
  return tasks.value
})
const stats=computed(()=>({
  total:tasks.value.length,
  done:tasks.value.filter(t=>t.done).length,
}))
const progres=computed(()=>({
progre:tasks.value.filter(t=>t.done).length/tasks.value.length *100
}))
function addTask(){
  if(newTask.value.trim()==='')return
  tasks.value.push({
    id:Date.now(),
    text:newTask.value,
    done:false,
  })
  newTask.value=''
}





</script>
 

<template>
  <div>
    <h1>Задачи на день</h1>
    <input v-model="newTask" placeholder="Новое задание" @keyup.enter="addTask" />
    <button @click="addTask">Добавить</button>
    <button @click="filter='all'">Все</button>
    <button @click="filter='active'">Активные</button>
    <button @click="filter='done'">Выполненные</button>
    <p>Выполнено:{{ stats.done }} из {{ stats.total }}</p>
    <P>Прогресс:{{ progres.progre}}%</P>
    <ul>
      <li v-for="task in visibleTasks" :key="task.id">
        <span :style="{textDecoration:task.done?'line-through':'none'}">{{ task.text }}</span>-{{ task.done?"✔":"X" }}
    
        <input v-model="task.done" type="checkbox" />


      </li>
    </ul>
  </div>
</template> -->




<!-- <script setup>
  import{ref,reactive, computed} from 'vue'
  const isVisible=ref(true)
  const students=ref([
    {
      id:1,
      name:"qwer",
      napr:"WEB-разработка",
      marks:4.3,
      age:18
    },
    {
      id:2,
      name:"asd",
      napr:"Программирование",
      marks:5.0,
      age:19
    },
    {
      id:3,
      name:"zxc",
      napr:"3D-дизайн",
      marks:3.5,
      age:10
    },
     {
      id:4,
      name:"vbvn",
      napr:"Девопсы",
      marks:4.5,
      age:31
    }
  ])
function addtStudent(){
  students.value.push({
      id:5,
      name:"tghfjh",
      napr:"-",
      marks:2.5,
      age:3122
    })
}

function deleteStudent(id){
    students.value=students.value.filter(student=>student.id!==id)
  }
</script>
 

<template>
  <div style="display: flex;justify-content: center;">
  <div v-for="student in students":key="student.id":style="{flexDirection:'column ',display:'flex',border:'1px solid white',width:'20%',marginRight:'40px',borderRadius:'10px'}">
    <h2>
      {{ student.name }}
    </h2>
    <h3>
      Возраст:{{ student.age }}
    </h3>
    <p>
      Средний балл:{{ student.marks }}
    </p>
    <h5>
      Направление:{{ student.napr }}
    </h5>  
    <button @click="deleteStudent(student.id)">remove</button>
  </div>
  
  </div>
  <button @click="addtStudent">Add</button>
</template>


<styles>

</styles> -->





<script setup>
  import{ref,reactive, computed} from 'vue'
 const name=ref(0)
 const text=ref('')
 const agree=ref(false)
 function showName(){
  alert(name.value+1)
 }
  function showText(){
  alert(text.value)
 }
</script>
 

<template>
  <input v-model.number="age" type="number" placeholder="Input name">
  <button @click="showName">Show</button>


   <textarea v-model="text"></textarea>
   <p>{{ text }}</p>
  <button @click="showText">Show</button>


  <label><input v-model="agree" type="checkbox">
    Я согласен
  </label>
  <p>{{ agree }}</p>
</template>
