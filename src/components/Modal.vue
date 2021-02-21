<template>
  <div class="taskContainer">
    <div class="modal"><slot name="model"></slot></div>
    <div v-on:click="set_modal">
      <Blur></Blur>
    </div>
  </div>
</template>
<script>
import Blur from "./Blur";
export default {
  name: "Modal",
  props: ["set_modal", "nameheight"],
  components: {
    Blur,
  },
};
</script>
<style scoped>
.taskContainer {
  width: 100%;
  height: 100vh;
  position: relative;
  background-color: rgba(255, 255, 255, 1);
  opacity: 100%;
  padding: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.modal {
  position: absolute;
  z-index: 999;
  background: #ffffff;
}
nameContainer {
  height: 50px;
}

@media screen and (max-width: 630px) {
  .taskContainer {
    width: auto;
    max-width: 400px;
  }
}
@media screen and (max-width: 500px) {
  .taskContainer {
    width: auto;
    max-width: 350px;

    justify-content: space-around;
    align-items: space-around;
  }
}
@media screen and (max-width: 500px) {
  .taskContainer {
    width: auto;
    max-width: 340px;

    justify-content: space-around;
    align-items: space-around;
  }
}
</style>
