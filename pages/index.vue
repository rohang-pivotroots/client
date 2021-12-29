<template>
  <!-- <Tutorial/> -->
  <div class="container ">
    <h1 class="header">API Integraion</h1>
    <p class="">This is a demo for api integration using Nuxt JS</p>
    <!-- <button class="btn btn-primary">Add Data</button> -->
    <section class="row no-gutters">
      <api-integration class="col-4" v-for="user in users" :key="user.username" :user="user"/>
    </section>
  </div>
</template>

<script>
export default {
  async fetch() {
    this.users = await fetch(
      'https://jsonplaceholder.typicode.com/users'
    ).then((res) => res.json())
  },
  data() {
    return {
      users: []
    }
  }
}
</script>
