<script>
import { reactive } from 'vue';

export default{
  setup(){
    const state = reactive({
  name: 'JG Souza Jr Dev',
  login: '',
  bio: '',
  company:'',
  avatar_url:'https://unsplash.it/258',
  searchInput: ''
});

async function fetchGithubUser(){
      const res = await fetch(`https://api.github.com/users/${state.searchInput}`);
      const {login, name, bio, company, avatar_url} = await res.json()

      state.login = login
      state.name = name
      state.bio = bio
      state.company = company
      state.avatar_url = avatar_url
   }

   return{
    state,
    fetchGithubUser
   }

  }
}


</script>

<template>    
  <main>
    <h1>GitHub User Data Método setup</h1>
  <input type="text" v-model="state.searchInput">
  <button @click="fetchGithubUser">Load User</button>
  <img :src="state.avatar_url">
  <strong>@{{state.login}}</strong>
  <h2>{{state.name}}</h2>
  <h3>{{state.company}}</h3>
  <span>{{state.bio}}</span>
  </main>
</template>