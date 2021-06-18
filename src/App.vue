<template>
  <div class="row">
    <div class="col" style="borderRight: 1px solid">
      <div class="col-title"><h1>TO DO</h1></div>
      <div class="col-content"><TaskCard v-bind:task="task" /></div>
    </div>
    <div class="col" style="borderRight: 1px solid">
      <div class="col-title"><h1>DOING</h1></div>

      <div class="col-content"><TaskCard v-bind:task="task" /></div>
    </div>
    <div class="col">
      <div class="col-title"><h1>DONE</h1></div>
      <div class="col-content"><TaskCard v-bind:task="task" /></div>
    </div>
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.css";
import TaskCard from "./components/TaskCard.vue";

var task = {
  header: "Header Task",

  text: "Lorem Ipsum Dolor Amet",
};

export default {
  name: "App",
  data: () => ({
    task: task,
  }),
  components: {
    TaskCard,
  },
};
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

.col-content {
  display: flex;
  justify-content: center;
}

.row {
  height: 100%;
}
</style>
