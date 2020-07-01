<template>
  <div class="home">
    <app-bar left='bars' right='search' title="TODO" />
    <avatar />
    <gradient />
    <TodoList />
    <todo-detail />
  </div>
</template>
<script>
import AppBar from './../components/AppBar'
import Avatar from './../components/Avatar'
import Gradient from './../components/Gradient'
import TodoList from './../components/TodoList'
import TodoDetail from './../components/TodoDetail'
export default {
  components: {
    AppBar,
    Avatar,
    Gradient,
    TodoList,
    TodoDetail
  }
}
</script>

<style lang="scss">
.home {
  height: 100%;
  width: 100%;
  overflow: hidden;
  color: white;
}
</style>