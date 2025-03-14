<template>
  
  <v-container style="max-width: 30%;">
    <v-list>
      <TareaLista v-for="tarea in tareas" :key="tarea.id" :tarea="tarea" />
    </v-list>
  </v-container>
</template>

<script>
import TareaLista from './TareaLista.vue'

export default {
  name: 'ListaTareas',
  components: {
    TareaLista
  },
  methods: {
    updateTareaEstado(newEstado) {
      const tarea = this.tareas.find(t => t.estado === newEstado);
      if (tarea) {
        tarea.estado = newEstado;
      }
    }
  },
  data() {
    return {
      tareas:[ {
        id: '1',
        titulo: 'Tarea 1',
        descripcion: 'Descripcion 1',
        estado: '0'
      },
      {
        id: '2',
        titulo: 'Tarea 2',
        descripcion: 'Descripcion 2',
        estado: '0'
      },
      {
        id: '3',
        titulo: 'Tarea 3',
        descripcion: 'Descripcion 3',
        estado: '0'
      },
      {
        id: '4',
        titulo: 'Tarea 4',
        descripcion: 'Descripcion 4',
        estado: '0'
      },
    ]

    };
  },
  
}
</script>

<style scoped>

</style>
