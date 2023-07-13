<script>
export default {
  data(){
    return{
      name: 'JG Souza Jr Dev',
      login: '',
      bio: '',
      company:'',
      avatar_url:'https://unsplash.it/256',
      searchInput: ''
    }
  },
  methods:{
    async fetchGithubUser(){
      const res = await fetch(`https://api.github.com/users/${this.searchInput}`);
      const {login, name, bio, company, avatar_url} = await res.json()

      this.login = login
      this.name = name
      this.bio = bio
      this.company = company
      this.avatar_url = avatar_url
   }
  }
}
</script>

<template>    
      <main>
        <h1>GitHub User Data</h1>
      <input type="text" v-model="searchInput">
      <button @click="fetchGithubUser">Load User</button>
      <img :src="avatar_url">
      <strong>@{{login}}</strong>
      <h2>{{name}}</h2>
      <h3>{{company}}</h3>
      <span>{{bio}}</span>
      </main>
</template>