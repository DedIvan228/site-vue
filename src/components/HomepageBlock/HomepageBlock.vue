<script setup>
import CalculatorBlock from '../CalculatorBlock/CalculatorBlock.vue'
import lenta from '../../assets/lenta.png'
</script>

<template>
<div class="homepage_wrapper">
    <div class="homepage structure">
        <div class="left-item">
            <div class="info_homepage">
                <h1>
                    <em>Установим лучший натяжной потолок </em><span class = "white">в Москве</span>
                </h1>
                <div class="main_text_homepage">
                    <p class="main_text">Используем только качественные, проверенные временем материалы. Сотрудничаем с
                        лучшими производителями натяжных потолков.</p>
                </div>
            </div>
        </div>
        <div class="guarantee">
            <div class="text_guarantee">
                <p>Устанавливаем натяжные потолки с 2015 года. <b>Честность и качество</b> <br>— залог успеха нашей
                    работы!</p>
            </div>
            <img :src="lenta" alt="" class = "picture_lenta">
        </div>
        <CalculatorBlock />
    </div>
</div>
</template>

<style scoped>
.homepage_wrapper {
    background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,1)),
    url(../../assets/background.png) center center;
    box-sizing: border-box;
    width: 100vw;
    background-size: cover;
}
.homepage {
    position: relative;
    font-family: 'Montserrat', sans-serif;
    display: flex;
    width: 80%;
    align-items: center;
    justify-content: space-between;
}
.homepage.structure {
    width: 63.5%;
    padding-top: 17.5rem;
    padding-bottom: 25.2rem;
}


/*текст (homepage -> left-item)*/
.left-item{
    position: relative;
    top: -5.7rem;
    left: -0.2rem;
    flex-direction: column;
    vertical-align: middle;
    width: 60rem;
}

.white{
    font-family: 'Montserrat', sans-serif;
    font-size: 3.44rem;
    color: white;
    font-weight: 600;
}
.info_homepage{
    max-width: 45rem;
}
.info_homepage h1{
    margin-bottom: 2.5rem;
    font-size: 3.44rem;
    width: 60rem;
}
.main_text{
    color: white;
    font-family: 'Montserrat', sans-serif;
    font-size: 1.929rem;
    width: 60rem;
}

h1{
    color: transparent;
    -webkit-background-clip: text;
    background-clip: text;
    background-image: linear-gradient(to right, #FEDA82, #FEC338);
}


/*гарантия*/
.guarantee{
    display:flex;
    flex-direction: column;
    position: absolute;
    width: min-content;
    align-items: center;
    text-align: center;
    bottom: 19.4rem;
    left: -0.265rem;
}
.text_guarantee{
    background-color: white;
    height: auto;
    width: 17.6rem;
    box-sizing: border-box;
    border-radius: 0.5rem;
    font-size: 0.96rem;
    padding: 0rem 1rem;
    padding-bottom: 2.9rem;
    margin-left: 0.1rem;

}
.picture_lenta{
    position: absolute;
    margin-left: -1.3rem;
    top: 6.3rem;
    width: 21rem;
}
</style>