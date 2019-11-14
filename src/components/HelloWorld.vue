<template>
  <div class="hello">
    <h1 id="heading">{{ msg }}</h1>
  </div>
</template>

<script>
let $ = window.jQuery;

export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  mounted: function() {
    $(this.$el)
      .find("#heading")
      .css("color", "red");
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/styles/_common.scss";
</style>
