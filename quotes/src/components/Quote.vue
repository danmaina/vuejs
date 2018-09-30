<template>
    <div class="col-md-4">
      <div class="panel panel-info">
        <div class="panel-body quote">
          <slot></slot>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  props: ["quotes"]
};
</script>

<style scoped>
.panel-body {
  font-family: "arizona", cursive;
  font-size: 1.5em;
  color: #6e6e6e;
}

.quote {
  cursor: pointer;
}

.quote:hover {
  background-color: #ffe2e2;
}

.panel-body {
  word-break: break-all;
}
</style>
