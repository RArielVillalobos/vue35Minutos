<template>
  <div>
    <p>Componente Hijo</p>
    <!--$emit nos permite emitir enventos a los componentes padres
        el payload son los datos que queremos emitir
      -->

    <button @click="$emit('clickChild','payload text')">{{btnText}}</button>

    <!-- otra forma de hacerlo-->
    <!-- luego declaramos el metodo-->
    <!--<button @click="fireEvent">Otra forma de click child</button> -->


  </div>
</template>

<script>
  // vamos a transmitir componentes desde componentes hijos a componentes padres
  export default {
    name:'ChildCmp',
    //usando props con la sintaxis de objetos podemos definir metadas como el type y si es requerido
    //podriamos tambien usar la notacion de array ['btnText']
    props: {
        btnText:{
          type:String,
          required:true

        }
    },

    methods:{
      fireEvent(){
        this.$emit('ClickChild','payload text 2');
      }
    }


  }
</script>
