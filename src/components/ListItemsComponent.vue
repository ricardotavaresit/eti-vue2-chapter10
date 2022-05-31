<template>
  <div>
    {{ title }}
    <ul>
      <li v-bind:key="index" v-for="(item, index) in items"> {{item}}</li>
    </ul>
  </div>

</template>

<script>
export default {
  props:{
    title:{
      required: true,
      type: String,
      default: ""
    },
    items:{
      required: true,
      type: Array,
      default: []
    }
  },
}

</script>


<style>
</style>
