<script setup>
</script>

<template>
<div class="slider-main">
    <p class="slider-text">Площадь потолка</p>
    <div class="slider-active">
        <input type="range" id="fader" class="range-first" min="1" max="200" value="1" step="1" >
        <output class="output" for="fader" id="volume">1 м2</output>
        <p class="min">01</p>
        <p class="max">200</p>
    </div>
</div>
</template>

<style scoped>
.slider-main{
    margin-bottom: 3.5rem;
    width: 29.8rem;
}
.slider-text{
    font-size: 1.4rem;
    font-weight: 500;
    margin-bottom: 0.5rem;
    width: auto;
    white-space: nowrap;
}
output{
    position: absolute;
    color:  #FEC338;
    font-size: 1.2rem;
    font-weight: bold;
    margin-top: 0.2rem;
    width: 6rem;
}
#fader{
    width: 29.8rem;
    height: 0.8rem;
}
.slider-active{
    border-radius: 0.4rem;
    width: 10rem;
    height: 0.8rem;
}
.min{
    margin-top: -0.25rem;
    position: absolute;
    font-size: 1.2rem;
    color: rgba(196, 196, 196, 0.644);
}
.max{
    position: absolute;
    margin-left: 27.6rem;
    margin-top: -0.25rem;
    font-size: 1.2rem;
    color: rgba(196, 196, 196, 0.644);
}
.range-first {
    -webkit-appearance: none;
    appearance: none;
    width: 22rem;
    height: 0.8rem;
    background: transparent;
}
.range-first::-webkit-slider-runnable-track {
    width: 100%;
    height: 0.7rem;
    background: rgba(196, 196, 196, 0.644);
    position: relative;
    border-radius: 1rem;
}
.range-first::-webkit-slider-thumb {
    -webkit-appearance: none;
    height: 1rem;
    width: 1rem;
    border-radius: 50%;
    background: #FEC338;
    margin-top: -0.1rem;
    position: relative;
    z-index: 0;
}
.range-first::-webkit-slider-runnable-track:before {
    content: "";
    display: block;
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    background-color: #FEC338;
    width: 100%;
    z-index: -100;
}
.range-first::-webkit-slider-runnable-track:after {
    content: "";
    display: block;
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    background-color: #FEC338;
    width: calc(100% - 20px);
    z-index: -200;
}
.range-first::-webkit-slider-thumb:hover::-webkit-slider-runnable-track:after,
.range-first::-webkit-slider-thumb:focus::-webkit-slider-runnable-track:after {
    background: black;
    z-index: 10000;
}
</style>