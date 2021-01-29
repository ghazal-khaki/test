<template>
  <div>
    {{`id:${child.id}`}}
    {{child.text}}
    <ul v-if="child.child">
      <Child
        :key="child.id"
        v-for="child in child.child"
        :child="child"
      >
      </Child>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'Child',
  props: {
    child: Object
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
