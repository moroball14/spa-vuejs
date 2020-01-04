<template>
  <div>
    <h2>User</h2>
    <router-link to="/users/1">Users1に行く</router-link>
    <router-link to="/users/2">Users2に行く</router-link>
    <hr>
    <h1>User No. {{id}}</h1>
  </div>
</template>

<script>
export default {
  props: ["id"]
}
</script>