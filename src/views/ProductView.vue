<template>
  <div class="container">
    <h1>This is an products page</h1>
    <div class="row">
      <div class="card" v-for="product in products" style="width: 18rem;" :key="product.id">
        <img :src="product.image" class="card-img-top" :alt="product.make">
        <div class="card-body">
          <h5 class="card-title">{{product.make}}</h5>
          <p class="card-text">{{product.spec}}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default{
  computed:{
    products(){
      return this.$store.state.products
    }
  },
  mounted(){
    this.$store.dispatch('fetchProducts')
  }
 
}
</script>
<style scoped>

</style>
