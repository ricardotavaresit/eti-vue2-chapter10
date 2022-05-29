<template>
  <div>
    {{ title }}
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
};
</script>

