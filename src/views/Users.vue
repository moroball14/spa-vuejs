<template>
  <div>
    <h2>User</h2>
    <router-link to="/users/1">Users1に行く</router-link>
    <router-link to="/users/2">Users2に行く</router-link>
    <hr>
    <h1>User No. {{id}}</h1>
    <router-link :to="'/users/' + (Number(id) + 1) + '/profile'">次のユーザー</router-link>
    <router-view></router-view>
    <div style="height: 1600px;"></div>
    <router-link id="next-user" :to="{ name: 'users-id-profile', params: { id: Number(id) + 1 } }">次のユーザー</router-link>
  </div>
</template>

<script>
export default {
  props: ["id"],
  // beforeRouteEnter(to, from, next){
  //   next(vm => {
  //     console.log(vm.id);
  //   });
  // },
  // beforeRouteUpdate(to, from, next){
  //   next()
  // },
  // beforeRouteLeave(to, from, next){
  //   const isLeave = window.confirm("本当にこのページを離れますか？");
  //   if (isLeave) {
  //     next()  
  //   } else {
  //     next(false)
  //   }
  // }
}
</script>