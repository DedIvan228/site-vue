<script setup>
import CalculatorBlockItem from './CalculatorBlockItem.vue'
import ABtnBlock from '../ABtnBlock/ABtnBlock.vue'
import line from '../../assets/line.png'
import calc from '../../assets/calc.png'
import icon from '../../assets/icon.png'
</script>

<template>
<div class="right-item">
            <div class="background_rectangle"></div>

            <div class="calculator">
                <div class="container"><h2>Расчёт стоимости</h2><img class="calculator_picture" :src="calc" alt=""></div>
                <CalculatorBlockItem text = "Площадь потолка" min = "01" max="200"/>
                <CalculatorBlockItem text = "Количество углов" min = "01" max="10"/>
                <CalculatorBlockItem text = "Количество светильников" min = "01" max="10"/>
                <div class="price-main">
                    <p class="price-text">Цена для вас</p>
                    <div class="price">
                        <img class="line" :src="line" alt="">
                        <div class="price-value">19 577<span class="currency">₽</span></div>
                    </div>
                </div>
                <img class="icon-phone" :src="icon" alt="" >
                <input class="phone-numbers" type="text" placeholder="Ваш номер телефона">
                <ABtnBlock />
            </div>
        </div>
</template>

<style scoped>
/*общие настройки калькулятора*/
.right-item {
    position: relative;
    display: flex;
    align-items: center;
    margin-top: -3.7rem;
}
.background_rectangle {
    position: absolute;
    background-color: white;
    width: 33.9rem;
    height: 45rem;
    border-radius: 1rem;
    left: 2rem;
    top: 0;
}
.calculator {
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
.container {
    display: flex;
    justify-content: space-between;
    height: 3rem;
    font-size: 1.5rem;
    font-weight: bold;
    margin-bottom: 2.05rem;
}
.calculator_picture {
    width: 13rem;
    height: 13rem;
    position: relative;
    margin-top: -4.4rem;
    right: 1.7rem;
    transform: rotate(-7deg)
}
h2 {
    font-size: 1.96rem;
    width: min-content;
    white-space: nowrap;
}

/*цена*/
.price-main {
    margin-top: -1.6rem;
    display: flex;
    height: 2rem;
    font-weight: 500;
    margin-bottom: 3.9rem;
    vertical-align: middle;
    text-align: center;
}
.price-text {
    width: min-content;
    white-space: nowrap;
    font-size: 1.45rem;
    padding: 0.2rem 0;
    margin-right: 2rem;
}
.price-value {
    margin-left: 1.3rem;
    margin-top: 1.1rem;
    width: min-content;
    font-size: 2.3rem;
    font-weight: 600;
}
.price {
    display: flex;
    width: min-content;
    white-space: nowrap;
    justify-content: space-between;
    vertical-align: middle;
    text-align: center;
}
.currency {
    position: absolute;
    margin-left: -0.2rem;
    margin-top: 1.2rem;
    font-size: 1.6rem;
}
.line {
    position: absolute;
    margin-top: 0.49rem;
    margin-left: -0.2rem;
    width: 11.9rem;
}

/*ввод телефона*/
.phone-numbers {
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
.icon-phone {
    margin-top: 1.5rem;
    margin-left: 1.1rem;
    position: absolute;
    width: 2.5rem;

}
</style>