<template>
  <div>
      <div v-if="index == 0" class="imagem">{{ index }}</div>
      <div v-if="index == 1" class="imagem">{{ index }}</div>
      <div v-if="index == 2" class="imagem">{{ index }}</div>
  </div>
</template>

<script>
export default {
    props: ['index']
}
</script>

<style>
    .imagem{
        height: 500px;
        width: 500px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 5rem;
        border: 1px solid black;
    }
</style>