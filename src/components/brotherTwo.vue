<template>
  <div class="teste">
      {{ chamada }}
  </div>  
</template>

<script>
import { bus } from '@/main';

export default {
    data(){
        return {
            chamada: ''
        }
    },
    created(){
        bus.$on('chamadaAlterada', (data) => {
            this.chamada = data
        })
    }
}
</script>

<style>
    .teste {
        margin: 10px;
        padding: 10px;
        border: 1px solid black;
    }
</style>