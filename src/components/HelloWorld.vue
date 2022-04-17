<template>
  <div class="HelloWorld">
    <h1>LISTA DE TAREAS</h1>
    <form class="formulario" @submit.prevent="addtareas">
      <label>
        TAREA:
        <input
          @keyup.enter="addtareas"
          type="text"
          placeholder="ingresa la tarea"
          v-model="AnotarTarea"
        />
      </label>
    </form>
    <button class="btn" @click="addtareas">Agreagar Tarea</button>
    <delete :tareas="tareas" @eliminar="deleteTareas" />
  </div>
</template>

<script>
import Delete from "./Delete.vue";
export default {
  data() {
    return {
      tareas: [],
      AnotarTarea: "",
    };
  },
  components: { Delete },
  methods: {
    addtareas() {
      this.tareas.push(this.AnotarTarea);
      this.AnotarTarea = "";
    },
    deleteTareas(index) {
      this.tareas.splice(index, 1);
    },
  },
};
</script>

<style>
.helloWorld {
  text-align: center;
  margin-top: 80px;
  padding: 40px;
}
.formulario {
  padding: 10px;
  font-size: 20px;
}
.btn {
  background: #00ffff;
  padding: 10px;
  margin-botton: 10px;
  border-radius: 5px;
  cursor: pointer;
}
</style>
