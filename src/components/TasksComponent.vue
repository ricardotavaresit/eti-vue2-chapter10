<template>
  <div>
    <h2>{{ title }}</h2>

    <input type="text" v-model="task" />

    <button v-on:click.prevent="callParent"> Call Father</button>


    <ul>
      <li v-bind:key="index" v-for="(item, index) in items" > {{ item }}</li>
    </ul>

  </div>
</template>


<script>
export default {
  props: ["items", "title"],
  data() {
    return {
      task:''
    };
  },
  methods:{
    callParent(){
      this.$emit('callParent', this.task)

      this.task = ''

    }
  }
};
</script>

