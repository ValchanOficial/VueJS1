<template>
  <div class="container">
    <div class="col-md-6 px-0 text-center">
      <h1>{{ title }}</h1>
      <ul class="list-group">
        <li class="list-group-item" v-for="img of imgs">
          <img :src="img.url" :alt="img.title"  class="img-fluid rounded">
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      title: 'Calopsita',
      imgs: [
        {
          url: './src/assets/dog.png',
          title: 'Dog'
        },
        {
          url: './src/assets/cat.jpg',
          title: 'Cat'
        }
      ]
    }
  }

}
</script>

<style>

</style>
