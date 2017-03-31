<template>
  <div class="container">
    <h1 class="centralized">{{ title }}</h1>
    
    <ul class="list-photos">
      <li class="list-photos-item" v-for="photo of photos">
        <my-panel :title="photo.title">
          <img class="img-responsive" :src="photo.url" :alt="photo.title">
        </my-panel>

      </li>
    </ul>
    
  </div>
</template>

<script>

import Panel from './components/shared/panel/Panel.vue';

export default {
  
  components: {
    'my-panel': Panel
  },

  data () {
    return {
      titulo: 'Alurapic', 

      photos: []
    }
  },
  created() {

    this.$http
      .get('http://localhost:3000/v1/fotos')
      .then(res => res.json())
      .then(photos => this.photos = photos, err => console.log(err));
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

</style>
