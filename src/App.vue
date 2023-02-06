<script>
import ColorPickerGame from "./components/ColorPickerGame.vue";
import Recap_01_02_2023 from "./components/Recap_01_02_2023.vue";

export default {
  components: { ColorPickerGame, Recap_01_02_2023 },
  data() {
    return {
      currentLesson: "color-picker-game",
    };
  },
};
</script>

<template>
  <div>
    <ColorPickerGame />
    <!-- <Recap_01_02_2023 /> -->
  </div>
</template>

<style scoped>
.total {
  display: flex;
  flex-direction: column;
}
</style>
