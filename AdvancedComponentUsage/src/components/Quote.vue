<template lang="html">
    <div class="">
        <!-- Slots -->
        <div class="">
            <slot name="title"></slot>
        </div>
        <hr>
        <div>
            <slot name="content"></slot>
        </div>
        <p>Quote</p>
    </div>
</template>

<script>
export default {
  props: ["quote"]
};
</script>

<style lang="css" scoped>
div {
  border: 1px solid #ccc;
  box-shadow: 1px 1px 2px black;
  padding: 30px;
  margin: 30px auto;
  text-align: center;
}

h2 {
  color: red;
}
</style>
