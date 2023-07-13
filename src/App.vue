<script>
import Github from './components/Github.vue'
export default {
components:{
  Github
}
}

</script>

<template>
  <Github/>
</template>

<style>
*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body{
  background: #1c1a1d;
  color: #e5e5e5;
}
#app{
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  min-height: 100vh;
  max-width: 40rem;
  margin: 0 auto;
  text-align: center;
}
img{
  display: block;
  border-radius: 999px;
  border: 1px solid #e5e5e5;
  margin: 1rem auto;
  width: 8rem;
  height: 8rem;
}
h1, h2{
  color: #f64348;
  margin: 1rem auto .25rem;  
}
h3{
  margin: 1rem auto .25rem;
}
span{
  display: block;
  margin: 1rem auto;  
}
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
a{
  color: #f64348;
}

</style>