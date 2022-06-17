<template>
  <Box>
    <div class="columns">
      <div class="column is-7">{{ tarefa.descricao || 'Tarefa sem descrição' }}</div>
      <div class="column">
        <Cronometro :tempoEmSegundos="tarefa.duracaoEmSegundos"/>
      </div>
    </div>
  </Box>
</template>

<script lang="ts">
import Cronometro from '@/components/Cronometro.vue'
import Box from '@/components/Box.vue'
import { defineComponent, PropType } from 'vue';
import ITarefa from '@/Interfaces/ITarefa';

export default defineComponent({
  name: "Tarefa-",
  components: {
    Cronometro,
    Box,
  },
  props: {
    tarefa: {
      type: Object as PropType<ITarefa>,
      required: true
    }
  }
});
</script>