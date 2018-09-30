<template>
    <div>
        <h3>The Author</h3>
    </div>
</template>

<script>
export default {
  deactivated() {
    console.log("deactivated");
  },
  activated() {
    console.log("activated");
  },
  destroyed() {
    console.log("destroyed");
  }
};
</script>

<style>
</style>
