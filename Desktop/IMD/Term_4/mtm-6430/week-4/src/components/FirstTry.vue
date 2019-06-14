<template>
  <div>
    <h2>
      This is my first try! My name is {{ name }} and I am {{ age }} years old.
    </h2>
    <ul>
      <li>Name: {{ name }}</li>
      <li>Age: {{ age }}</li>
      <li>Color: {{ color }}</li>
      <li>{{ treat }}</li>
    </ul>
  </div>
</template>
<script>
export default {
  props: ["treat"],
  data: function() {
    return {
      name: "Daniel",
      age: 6,
      color: "Black"
    };
  }
};
</script>
<style lang="scss">
h2 {
  color: red;
}
</style>
