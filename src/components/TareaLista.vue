<template>
  <v-list-item :title="tarea.titulo" :subtitle="tarea.descripcion" class="item">   
      <template v-slot:append>
        <v-checkbox />
        </template>
  </v-list-item>
</template>

<script>
export default {
  name: 'TareaLista',
  props : {
    tarea: {
      type: Object,
      required: true 
    },
  },
  methods: {
    updateEstado() {
      this.$emit('update:tareaEstado', this.tarea.estado);
    }
  }

}
</script>

<style scoped>
  .item{
    border: 1px solid #333131;
    border-radius: 10px;
  }
</style>
