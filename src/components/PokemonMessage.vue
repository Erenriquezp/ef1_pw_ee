<template>
   <div v-if="mensaje" class="message-container">
      <p  :style="{color: color}">
         {{mensaje}}
      </p>
      <button @click="$emit('reiniciar')" class="btn-container">Nuevo Juego</button>
   </div>
</template>

<script>
export default {
   props: ['mensaje', 'color', 'reiniciar'],
}
</script>

<style>
   .message-container {
      margin: 10px;
      padding: 10px;
      font-weight: bold;
      font-size: 20px;
      border: 1px solid black;
   }
</style>



