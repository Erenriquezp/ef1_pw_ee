<template>
   <div class="square-container">
      <div>
         <img :src="imagenSrc" alt="Pokemon"></img>
      </div>
      <p> {{ nameSrc }}</p>
   </div>
</template>

<script>
export default {
   props: ['imagen', 'name'],
   computed: {
      imagenSrc() {
         return this.imagen ? this.imagen : 'https://dummyimage.com/250x250'
      },
      nameSrc() {
         return this.name ? this.name : 'XXXXXXXXXXXXX'
      }
   }
}
</script>

<style scoped>
   .square-container {
      display: flex;
      flex-direction: column;
      margin: 30px;
   }
   img {
      width: 150px;
      height: 150px;
   }
</style>

