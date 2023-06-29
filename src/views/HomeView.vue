<template>
  <div class="home">
    <form @submit.prevent="displayData">
      <div>
        <input type="text" v-model="firstName" placeholder="firstName" required>
      </div>
      <div>
      <input type="text" v-model="lastName" placeholder="lastName" required>
      </div>
      <div>
        <!-- <label>{{firstName}}-{{lastName}}</label> -->
        <label id="output"></label>
      </div>
      <div><button @click="displayData">Submit
      </button></div>
    </form>
    </div>

 
</template>

<script>
  export default {
    name:'HomeView',
    components:{
    },
    data(){
      return{
        firstName:'',
lastName:''
    
      }
    },
      methods:{
        displayData(){
          document.querySelector('#output').textContent=`${this.firstName}${this.lastName}`
        }
      }
    
  }
</script>

<style scoped>

</style>