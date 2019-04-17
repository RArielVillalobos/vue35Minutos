<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
   <input v-model="msg">
    <button @click="hello(msg)">Click Here</button>
    <br>
    <!-- tambien podemos usar esto como evento con parametro tambien se le puede pasar parametros a @click -->
    <button v-on:click="hello(msg)">Otro Click</button>
    <br>
    <button @click="toggleShow">Cambiar valor </button>
    <br>
    <p>{{this.name}}</p>
    <!--  tambien lo podemos hacer asi-->
    <p>{{apellido}}</p>

    <p>Metodo computado</p>
    {{fullName}}

    <!--  condicionales-->
    <p v-if="edad>=18">Sos mayor de edad</p>

    <p v-else>No sos mayor de edad</p>

    <!--  condicionales-->
    <p v-if="show==1">{{fullName}}</p>

    <p v-else>no se muestra</p>

    <p>Contenido evento click hijo</p>


    <!-- como Recuperar la info de los datos del evento hijo-->
    <!-- el eventoClickChild puede llevar otro nombre, con $event traemos los datos el payload-->
    <!--Ahora declaramos esta funcion en los metodos -->
    <child-cmp @clickChild="eventClickChild($event)" :btnText="btnText"></child-cmp>
    <br>

   <users-list />

  </div>
</template>

<script>
import ChildCmp from './ChildCmp';

import UsersList from "./UsersList";


export default {
  name: 'HelloWorld',
  components: {UsersList, ChildCmp},
  data () {
    return {
      msg: '',
      name:'ariel',
      apellido:'villalobos',
      edad:12,
      show:false,
      btnText: 'pulsarr el boton'
    }
  },
  methods:{
    hello(msg){
      alert('clickeaste: '+msg);
    },
    toggleShow(){

     this.show=!this.show;
    },
    eventClickChild($event){
      console.log($event);
    }



  },
  //los metodos computados vue los convierte en variable entonces son mas facil para acceder
  computed:{
    fullName(){
      return this.name+this.apellido;
    },
    eventClickChildTwo($event){
      console.log($event);
    },
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
p{
  color:red
}
</style>
