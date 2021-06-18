<template>
  <div class="card">
    <div class="card-header">
      {{ task.header }}
    </div>
    <div class="card-body">
      <p class="card-text">
        {{ task.text }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "TaskCard",
  props: ["task"],
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card {
  background: gray;
  border: 1px solid;
  width: 250px;
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
}

.card-header {
  font-weight: 700;
  background: lightgray;
  height: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.card-body {
  color: white;
}
</style>
