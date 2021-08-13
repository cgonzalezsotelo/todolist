<template>
  <form id="tareas">
    <h2>Crar una nueva tarea</h2>
    <label>Tarea</label>
    <input type="text" v-model="nuevaTarea" placeholder="Ingresa una nueva tarea">
    <button v-on:click.prevent="agregarNuevaTarea">Crear</button>
    <h2>Lista</h2>
    <ul>
      <li v-for="(tarea, index) in tareas" :key="index">
        {{index}}: {{tarea}}
      </li>
    </ul>
  </form>
</template>

<script>

export default {
  name: 'App',
  data: () => ({
    nuevaTarea: "",
    tareas: []   
  }),
  methods: {
    agregarNuevaTarea(){
      this.tareas.push(this.nuevaTarea)
      this.nuevaTarea = ""    
    }
  }

}
</script>

<style>
</style>
