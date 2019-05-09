<template>
  <div class="hello col-lg-4 mx-auto">
      <div>
        <div class="mt-2">Naziv knjige {{ text }}</div>
        <b-form-input v-model="knjiga" placeholder="Unesi Naziv knjige"></b-form-input>
      </div>
      <div>
        <div class="mt-2">autor: {{ text }}</div>
        <b-form-input v-model="autor" placeholder="Unesi Naziv autora"></b-form-input>
      </div>
      <div>
        <div class="mt-2">Izdavac: {{ text }}</div>
        <b-form-input v-model="izdavac" placeholder="Unesi Naziv izdavaca"></b-form-input>
      </div>
      <div>
        <div class="mt-2">Zanr: {{ text }}</div>
        <b-form-input v-model="zanr" placeholder="Unesi Naziv zanra"></b-form-input>
      </div>
      <b-button variant="success" class="mt-2">Posalji</b-button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
      return {
        knjiga: '',
        autor:'',
        izdavac:'',
        zanr:''
      }
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
