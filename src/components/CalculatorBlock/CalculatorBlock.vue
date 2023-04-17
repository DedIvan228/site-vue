<script setup>
</script>

<template>
<div class="right-item">
            <div class="background_rectangle"></div>

            <div class="calculator">
                <div class="container"><h2>Расчёт стоимости</h2><img class="calculator_picture" src="../../assets/calc.png" alt="" width="100px" height="100px"></div>
                <div class="slider-main">
                    <p class="slider-text">Площадь потолка</p>
                    <div class="slider-active">
                        <input type="range" id="fader" class="range-first" min="1" max="200" value="1" step="1"
                               oninput="outputUpdate(value); range()">
                        <output class="output" for="fader" id="volume">1 м2</output>
                        <p class="min">01</p>
                        <p class="max">200</p>
                    </div>
                </div>
                <div class="slider-main">
                    <p class="slider-text">Количество углов</p>
                    <div class="slider-active">
                        <input type="range" id="fader" class="range1" min="1" max="10" value="1" step="1"
                               oninput="outputUpdate1(value); range()">
                        <output class="output1" for="fader1" id="volume1">1</output>
                        <p class="min1">01</p>
                        <p class="max1">10</p>
                    </div>
                </div>
                <div class="slider-main">
                    <p class="slider-text">Количество светильников</p>
                    <div class="slider-active">
                        <input type="range" id="fader" class="range2" min="1" max="10" value="1" step="1"
                               oninput="outputUpdate2(value); range()">
                        <output class="output2" for="fader2" id="volume2">1</output>
                        <p class="min1">01</p>
                        <p class="max1">10</p>
                    </div>
                </div>
                <div class="price-main">
                    <p class="price-text">Цена для вас</p>
                    <div class="price">
                        <img class="line" src="../../assets/line.png" alt="">
                        <div class="price-value">19 577<span class="currency">₽</span></div>
                    </div>
                </div>
                <img class="icon-phone" src="../../assets/icon.png" alt="" >
                <input class="phone-numbers" type="text" placeholder="Ваш номер телефона">
                <div class="button" href=""><p class="tex">отправить заявку</p></div>
            </div>
        </div>
</template>

<style scoped>
/*общие настройки калькулятора*/
.right-item{
    position: relative;
    display: flex;
    align-items: center;
    margin-top: -3.7rem;
    left: -2rem;
}
.background_rectangle{
    position: absolute;
    background-color: white;
    width: 33.9rem;
    height: 45rem;
    border-radius: 1rem;
    left: 2rem;
    top: 0;
}
.calculator{
    position: relative;
    background-color: white;
    width: 37.9rem;
    height: 44rem;
    border-radius: 1rem;
    z-index: 1;
    box-shadow: 0.02rem 0.02rem 0.25rem;
    padding: 0.35rem 4.19rem;
    box-sizing: border-box
}
.container{
    display: flex;
    justify-content: space-between;
    height: 3rem;
    font-size: 1.5rem;
    font-weight: bold;
    margin-bottom: 2.05rem;
}
.calculator_picture{
    width: 13rem;
    height: 13rem;
    position: relative;
    margin-top: -4.4rem;
    right: 1.7rem;
    transform: rotate(-7deg)
}
h2{
    font-size: 1.96rem;
    width: min-content;
    white-space: nowrap;
}


/*первый слайдер*/
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


/*второй слайдер*/
.min1{
    margin-top: -0.25rem;
    position: absolute;
    font-size: 1.2rem;
    color: rgba(196, 196, 196, 0.644);
}
.max1{
    margin-top: -0.25rem;
    font-size: 1.2rem;
    position: absolute;
    margin-left: 28.5rem;
    color: rgba(196, 196, 196, 0.644);
}
.output1{
    position: absolute;
    color:  #FEC338;
    font-size: 1.2rem;
    font-weight: bold;
    margin-top: 0.1rem;
    margin-left: 0.2rem;
}
#fader1{
    width: 29.8rem;
    height: 0.8rem;
}
.range1 {
    -webkit-appearance: none;
    appearance: none;
    width: 100%;
    height: 0.8rem;
    background: transparent;
}
.range1::-webkit-slider-runnable-track {
    width: 100%;
    height: 0.8rem;
    background: rgba(196, 196, 196, 0.644);
    position: relative;
    border-radius: 1rem;
}
.range1::-webkit-slider-thumb {
    -webkit-appearance: none;
    height: 1rem;
    width: 1rem;
    border-radius: 50%;
    background: #FEC338;
    top: -0.1rem;
    position: relative;
    z-index: 0;
}
.range1::-webkit-slider-runnable-track:before {
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

.range1::-webkit-slider-runnable-track:after {
    content: "";
    display: block;
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    background-color: rgba(196, 196, 196, 0.644);
    width: calc(100% - 20px);
    z-index: -200;
}
.range1::-webkit-slider-thumb:hover::-webkit-slider-runnable-track:after,
.range1::-webkit-slider-thumb:focus::-webkit-slider-runnable-track:after {
    background: black;
    z-index: 10000;
}



/*третий слайдер*/
.output2{
    position: absolute;
    color:  #FEC338;
    font-size: 1.2rem;
    font-weight: bold;
    margin-top: 0.1rem;
    margin-left: 0.2rem;
}
#fader2{
    position: relative;
    width: 29.8rem;
}
.range2 {
    -webkit-appearance: none;
    appearance: none;
    width: 100%;
    height: 0.8rem;
    background: transparent;
}

.range2::-webkit-slider-runnable-track {
    width: 100%;
    height: 0.8rem;
    background: rgba(196, 196, 196, 0.644);
    position: relative;
    border-radius: 20px;
}

.range2::-webkit-slider-thumb {
    -webkit-appearance: none;
    height: 1rem;
    width: 1rem;
    border-radius: 50%;
    background: #FEC338;
    margin-top: -0.1rem;
    position: relative;
    z-index: 0;
}

.range2::-webkit-slider-runnable-track:before {
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

.range2::-webkit-slider-runnable-track:after {
    content: "";
    display: block;
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    background-color: rgba(196, 196, 196, 0.644);
    width: calc(100% - 20px);
    z-index: -200;
}

.range2::-webkit-slider-thumb:hover::-webkit-slider-runnable-track:after,
.range2::-webkit-slider-thumb:focus::-webkit-slider-runnable-track:after {
    background: black;
    z-index: 10000;
}


/*цена*/
.price-main{
    margin-top: -1.6rem;
    display: flex;
    height: 2rem;
    font-weight:500;
    margin-bottom: 3.9rem;
    vertical-align: middle;
    text-align: center;
}
.price-text{
    width: min-content;
    white-space: nowrap;
    font-size: 1.45rem;
    padding: 0.2rem 0;
    margin-right: 2rem;
}
.price-value{
    margin-left: 1.3rem;
    margin-top: 1.1rem;
    width: min-content;
    font-size: 2.3rem;
    font-weight: 600;
}
.price{
    display: flex;
    width: min-content;
    white-space: nowrap;
    justify-content: space-between;
    vertical-align: middle;
    text-align: center;
}
.currency{
    position: absolute;
    margin-left: -0.2rem;
    margin-top: 1.2rem;
    font-size: 1.6rem;
}
.line{
    position: absolute;
    margin-top: 0.49rem;
    margin-left: -0.2rem;
    width: 11.9rem;
}


/*ввод телефона*/
.phone-numbers{
    width: 21.2rem;
    margin-left: 0.1rem;
    height: 5rem;
    border-radius: 0.75rem;
    padding: 0 4rem;
    border: rgba(216, 216, 216, 0.301);
    background-color: rgba(216, 216, 216, 0.301);
    font-size: 1.2rem;
    border: 0.05rem solid rgb(197, 197, 197);
    margin-bottom: 1.139rem;

}
.icon-phone{
    margin-top: 1.5rem;
    margin-left: 1.1rem;
    position: absolute;
    width: 2.5rem;

}


/*кнопка*/
.button{
    width: 29.4rem;
    height: 5.39rem;
    margin-left: 0.1rem;
    padding: 0.5rem 0;
    box-sizing: border-box;
    background-image: linear-gradient(to bottom,#FEDA82, #FEC338);
    border-radius: 1.3rem;
    text-decoration: none;
    color: black;
    box-shadow: 0 0.15rem 0 rgba(73, 20, 20, 0.342);
    text-align: center;
}
.tex{
    margin-right: 0.6rem;
    font-size: 1.36rem;
}
</style>