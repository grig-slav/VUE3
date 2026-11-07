<script setup>
import{ref} from 'vue'

</script>
<template>
    <div>
         <h1 class="zag">КРУТОЙ САЙТ</h1>
         <nav class="mainNav">
          <a    class='navLink' href="">
            Календарь путешествий
          </a>

          <a  class='navLink' href="">
            Аренда техники
          </a> 
          <a  class='navLink' href="">
            Команда
          </a>
          <a  class='navLink' href="">
            Сертификаты
          </a>
        </nav>

        
   </div>
</template>
<style scoped>
.mainNav {
  display: flex;
  align-items: center;
  background: rgba(0, 0, 0, 0.5);
  backdrop-filter: blur(12px);
  padding: 10px clamp(12px, 2vw, 30px);
  border-radius: 10px;

 
}
.navLink {
  color: #ffffff;
  text-decoration: none;
  font-size: clamp(13px, 1.1vw, 19px);
  font-weight: 300;
  padding: 8px 10px;
  transition: color 0.2s ease;
  white-space: nowrap;
}
.zag{
    display: flex;
    align-items: center;
    justify-content: center;
}
</style>