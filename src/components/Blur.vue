<template>
  <div class="blur"><slot></slot></div>
</template>
<script>
export default {
  name: "Blur",
};
</script>
<style scoped>
.blur {
  position: absolute;
  z-index: 1;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  display: flex;

  justify-content: "center";
  box-sizing: border-box;

  background-color: black;
  opacity: 0.7;
}
</style>
