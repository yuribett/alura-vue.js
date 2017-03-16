<template>
  <div>
    <h1>{{ title }}</h1>
    <ul v-for="photo of photos">
      <li><img :src="photo.url" :alt="photo.title"></li>
    </ul>
    
  </div>
</template>

<script>
export default {
  
  data () {
    return {
      title: 'Alurapic',
      photos: [{
        title: 'Dog',
        url: 'http://tudosobrecachorros.com.br/wp-content/uploads/cachorro-independente.jpg'
      }]
    }
  }
}
</script>

<style lang="scss">

</style>
