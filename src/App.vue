<template>
  <div id="app">
    <h1>{{ msg }}</h1>
    <tasks-component v-bind:items="['Task 1', 'Task 2', 'Task 3']" v-bind:title="'Best Task List '" v-on:callParent="answerSon" />
    <listItems-component v-bind:title="'List of...'" v-bind:items="['Value 1', 'Value 2', 'Value 3']"/>
    <listItems-component v-bind:title="'List of products'" v-bind:items="['Product 1', 'Product 2', 'Product 3']"/>
  </div>
</template>

<script>
import TasksComponent from "./components/TasksComponent";
import ListItemsComponent from "./components/ListItemsComponent";

export default {
  name: "app",
  data() {
    return {
      msg: "Welcome to Your Vue.js App"
    };
  },
  components: {
    TasksComponent,
    ListItemsComponent
  },
  methods:{
    answerSon(){
      alert("answerSon");
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
