<script setup>
import{ref} from 'vue';
  const emit = defineEmits(['formSubmit'])
  const searchInput = ref('')

  function handleSubmit(ev){
    ev.preventDefault()
    emit('formSubmit', searchInput.value)
  }
</script>

<template>
  <form @submit="handleSubmit" >
      <input type="text" v-model="searchInput">
      <button >Load User</button>
  </form> 
</template>

<style scoped>
input, button{
  max-width: 20rem;
  padding: .5rem;
}
input{
  background: #1c1a1d;
  border: 1px solid #f64348;
  border-radius: .25rem;
  color: #e5e5e5;
  margin: 1rem 1rem 1rem 0;
}
button{
  background: #f64348;
  border: unset;
  border-radius: .25rem;
  color: #1c1a1d;
  font-size: 1rem;
  font-weight: 700;
  text-transform: uppercase;
}
button:hover{
  cursor: pointer;
  filter: brightness(.95);
}
</style>