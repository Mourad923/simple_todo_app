<template>
    <div>

         {{ todos }}
       
      <todos v-model="todos"></todos>
  
      <todos></todos>

      <button @click="addTodo">Ajouter une tache</button>

    </div>  
</template>

<script>
import Todos from './components/Todos'

export default {
  data(){

    return{

      todos: [{

        name:'Demo',
        completed:true
      }]
    }
  },

  methods: {
    addTodo () {

      this.todos.push({

        name:'jean',
        completed:false
      })
    }
  },
  components: {
    Todos
  }
}
</script>

<style>
html {
  height: 100%;
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

#app {
  color: #2c3e50;
  margin-top: -100px;
  max-width: 600px;
  font-family: Source Sans Pro, Helvetica, sans-serif;
  text-align: center;
}

#app a {
  color: #42b983;
  text-decoration: none;
}

.logo {
  width: 100px;
  height: 100px
}
</style>
