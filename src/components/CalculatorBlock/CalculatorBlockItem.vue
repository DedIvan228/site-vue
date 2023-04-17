<script setup>
function outputUpdate2(val) {
    var output = document.querySelector('#volume2');
    output.value = val;
    output.style.left = val * 3.2 + 1 + 'rem';
}

let CalculatorBlockItemProps = {
  min: Number,
  max: Number
}
const props = defineProps(CalculatorBlockItemProps)

</script>

<template>
  <div class="slider-main">
    <p class="slider-text">Площадь потолка</p>
    <div class="slider-active">
      <input type="range" class="fader range-first" :min="min" :max="max" value="1" step="1"
        oninput="outputUpdate(value, '.fader'); range()">
      <output class="output" for="fader" id="volume">1 м2</output>
      <p class="min">{{ min }}</p>
      <p class="max">{{ max }}</p>
    </div>
  </div>
</template>

<style scoped>

</style>