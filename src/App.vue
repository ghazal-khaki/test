<template>
  <div id="app">
    <Child
      :key="data.id"
      v-for="data in arrayOfData"
      :child="data"
    />
  </div>
</template>

<script>
import Child from './components/Child.vue'

export default {
  name: 'App',
  data () {
    return {
      arrayOfData: [
        {
          id: 1,
          text: "text1",
          child: [
            {
              id: 2,
              text: "text2",
              child: null
            },
            {
              id: 3,
              text: "text3",
              child: [
                {
                  id: 4,
                  text: "text4",
                  child: null
                },
                {
                  id: 5,
                  text: "text5",
                  child: null
                }
              ]
            }
          ]
        },
        {
          id: 6,
          text: "text6",
          child: [
            {
              id: 7,
              text: "text7",
              child: null
            },
            {
              id: 8,
              text: "text8",
              child: [
                {
                  id: 9,
                  text: "text9",
                  child: null
                },
                {
                  id: 10,
                  text: "text10",
                  child: [
                    {
                      id: 11,
                      text: "text11",
                      child: null
                    },
                    {
                      id: 12,
                      text: "text12",
                      child: null
                    }
                  ]
                }
              ]
            }
          ]
        }
      ]
    }
  },
  components: {
    Child
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
