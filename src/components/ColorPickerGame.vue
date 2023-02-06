<template>
  <h1 class="header">Color Picker Game</h1>

  <div class="mes-cont">
    <div class="msg">
      {{ message }}
    </div>

  </div>

  <div class="btn-container">
    <button
      v-for="color in colors"
      :key="color"
      @click="matchColor(color)"
      class="btn"
      :style="{color: `${color}`}"
    >
      {{ color }}
    </button>
  </div>
</template>

<script>
import ColorPicker from "../composables/color-picker-assigment";

export default {
  setup() {
    const { colors, message, matchColor } = ColorPicker();
    return { colors, message, matchColor };
  },
};
</script>

<style>
.header {
  text-align: center;
  font-size: 2.5rem;
  font-weight: 500;
  margin-bottom: 5rem;
}

.mes-cont {
position: relative;
left: 17%;
}

.msg {
  text-align: center;
  width: 20rem;
  border: 4px solid white;
  border-radius: 5px;
  box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.2);
}
.btn-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.btn {
  width: 1rem;
  height: 1rem;
  border: none;
  border-radius: 20px;
  margin: 1rem;
  font-size: 1.5rem;
  font-weight: 700;
  cursor: pointer;
}

@media screen and (min-width: 768px) {
  .btn {
    width: 150px;
    height: 150px;
    font-size: 2rem;
  }
  .header {
    font-size: 2.5rem;
  }

  .msg {
    font-size: 1.5rem;
  }
}
</style>
