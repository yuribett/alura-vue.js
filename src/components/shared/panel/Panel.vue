<template>

    <div class="panel">
        <h2 class="panel-title">{{ title }}</h2>
        <div class="panel-body">
            <slot class="panel-content">
            </slot>
        </div>
    </div>

</template>

<script>
export default {
    props: ['title']

}
</script>

<style scoped>

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

  * {
    box-shadow: 5px 5px 5px;
  }
</style>