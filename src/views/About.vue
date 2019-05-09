<template>
  <div class="about col-lg-8 mx-auto">
    <b-list-group>
      <div class="container">
      <b-list-group-item v-for="(post,i) in posts" :key="i">
        <div class="row">
        <div class="col-lg-4" style="my-auto">
          <img :src="post.thumbnailUrl" alt="post.title" class="my-auto">
        </div>
        <div class="col-lg-8 text-left">
          <h3>{{post.title}}</h3>
          <p>Autor: Matija Beckovic</p>    
          <p>Prodavnica: LeoCommerce</p>    
          <p>Cena: 1200RSD</p>    
        <b-button variant="danger" class="mt-auto" style="float:right;">Naruci</b-button>  
        </div>      
        </div>
        </b-list-group-item>
      </div>
    </b-list-group>
  </div>
</template>


<script>
export default {
  name: 'HelloWorld',
  data() {
      return {
        posts:[]
      }
    },
    mounted(){
      axios.get('https://jsonplaceholder.typicode.com/photos')
      .then(response => {
        for (let i = 0; i < 10; i++) {
          this.posts.push(response.data[i]);
        }
        console.log(this.posts);
        
      })
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
