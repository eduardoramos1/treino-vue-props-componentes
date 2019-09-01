<template>
  <div class="teste" @click="mudarChamada">
      {{chamada}}
  </div>   
</template>

<script>
import { bus } from '@/main'; 

export default {
    data(){
        return {
            chamada: 'blabla'
        }
    },
    methods: {
        mudarChamada(){
            bus.$emit('chamadaAlterada', this.chamada)
        }
    }
}
</script>

<style>

</style>