<template>
  <div class="container">
    <h1 class="centralized">{{ title }}</h1>
    
    <ul class="list-photos">
      <li class="list-photos-item" v-for="photo of photos">
        <div class="panel">
          <h2 class="panel-title">{{photo.title}}</h2>
          <div class="panel-body">
            <img class="img-responsive" :src="photo.url" :alt="photo.title">
          </div><!-- fim panel-body -->
        </div><!-- fim panel -->
      </li>
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
  .centralized {
    text-align: center;
  }

  .container {
    font-family: Helvetica, sans-serif;
    margin: 0 auto;
    width: 96%;
  }

  .list-photos {
    list-style: none;
  }

  .list-photos .list-photos-item {
    display: inline-block;
  }

  .img-responsive {
    width: 95%;
  }

  .panel {
    padding: 0 auto;
    border: solid 2px grey;
    display: inline-block;
    margin: 5px;
    box-shadow: 5px 5px 10px grey;
    width: 200px;
    height: 100%;
    vertical-align: top;
    text-align: center;
  }

  .panel .panel-title {
    text-align: center;
    background: lightblue;
    margin: 0 0 15px 0;
    padding: 10px;
    text-transform: uppercase;
  }

</style>
