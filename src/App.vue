<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <ul>
      <TreeItem class="item" :item="treeData" />
    </ul>
    <BookList :books="books" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import TreeItem from "./components/TreeItem.vue";
import BookList from "./components/BookList.vue";

export default {
  name: "app",
  data: function() {
    return {
      treeData: {
        name: "My Tree",
        children: [
          { name: "hello" },
          { name: "wat" },
          {
            name: "child folder",
            children: [
              {
                name: "child folder",
                children: [{ name: "hello" }, { name: "wat" }]
              },
              { name: "hello" },
              { name: "wat" },
              {
                name: "child folder",
                children: [{ name: "hello" }, { name: "wat" }]
              }
            ]
          }
        ]
      },
      books: [
        { id: 1, title: "Bla", author: "blabla" },
        { id: 2, title: "Bla", author: "blabla" },
        { id: 3, title: "Bla", author: "blabla" },
        { id: 4, title: "Bla", author: "blabla" },
        { id: 5, title: "Bla", author: "blabla" }
      ]
    };
  },
  components: {
    HelloWorld,
    TreeItem,
    BookList
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
