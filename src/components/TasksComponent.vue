<template>
  <div>
    <h2>{{ title }}</h2>

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

    };
  },
  methods:{
    callParent(){
       alert("callParent");
      this.$emit('callParent')
    }
  }
};
</script>

