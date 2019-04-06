<template>
  <table>
    <tr>
      <th>name</th>
      <th>id</th>
      <th>phone</th>
      <th>age</th>
    </tr>
    <tr v-for="(user,i) in userTable" :key="`user-${i}`">
      <td>{{user.name}}</td>
      <td>{{user.id}}</td>
      <td>{{user.phone}}</td>
      <td>{{user.age}}</td>
    </tr>
  </table>
</template>

<script>
import userTable from "@/store/data"

export default {
  name: 'UserList',
  data(){
    return {
      userTable
    }
  }
}
</script>

<style scoped>
  table {
    border-collapse: collapse;
  }
  th,td{
    border: 1px solid gray;
    padding: 5px
  }
</style>

