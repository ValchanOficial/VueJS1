<template>
  <div class="container">
    <div class="col-md-4 px-0 text-center">
        <img v-for="img of imgs" :src="img.url" :alt="img.title"  class="img-thumbnail border img-fluid rounded">
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      imgs: []
    }
  },
  created() {
    this.$http.get('http://localhost:3000/v1/fotos')
      .then(res => res.json())
      .then(imgs => this.imgs = imgs, err => console.log(err)); //res.json // imgs // imgs.json
  }
}
</script>

<style>

</style>
