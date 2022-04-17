<template>
  <div class="Delete">
    <ul v-if="tareas.length > 0">
      <li class="li" v-for="(tarea, index) in tareas" :key="index">
        {{ index + 1 }} {{ tarea }}
        <button class="btnoff" @click="btnDelete(index)">Eliminar</button>
      </li>
    </ul>
    <p v-else>No hay tareas el dia de hoy</p>
  </div>
</template>

<script>
export default {
  name: "DeleteDelete",
  props: {
    tareas: {
      type: Array,
    },
  },
  methods: {
    btnDelete(index) {
      this.$emit("eliminar", index);
    },
  },
};
</script>

<style>
.li {
  list-style: none;
  padding: 5px;
}
.btnoff {
  background: #00ffff;
  border-radius: 5px;
}
</style>
