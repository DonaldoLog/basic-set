<template lang="pug">
  #app
    img(src="./assets/logo.png")
    h1 {{ dato }}
    button(@click="agregar") Agregar prop
    button(@click="agregarSet") Agregar prop usando set
    button(@click="agregarECM") Agregar prop usando ecm
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      dato: {
        nombre: 'Donaldo'
      }
    }
  },
  methods: {
   agregar(){
     this.dato.primerAp = 'Lopez' 
     console.log(1);
   },
   agregarSet(){
     this.$set(this.dato, 'primerAp', 'Lopez')
     console.log(2);
   },
   agregarECM(){
     this.dato = Object.assign({},this.dato, {segundoAp: 'Gil'})
   }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
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
