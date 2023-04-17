<script setup>

</script>

<template>
<div class="header clearfix">
    <div class="structure">
        <div class="header-logo">
            <div class="logo">
                <p class="t_l">лого</p>
            </div>
            <div class="name">
                Натяжные потолки в Москве
            </div>
        </div>
        <div class="header-contact">
            <div class="schedule">Пн-Вс. 8:00–22:00</div>
            <div class="contacts">
                <img class="icon_wa" alt="Whatsapp" src="../../assets/whatsapp.jpg">
                <p class="WA">Написать в WhatsApp</p>
            </div>
        </div>
    </div>
</div>
</template>

<style scoped>
.header{
    font-family: 'Montserrat', sans-serif;
    position: fixed;
    top: 0rem;
    left: 0rem;
    z-index: 10000;
    width: 100%;
    background: #0000004d;
}

.header .structure {
    display: flex;
    padding: 3.8rem 11.2rem;
    padding-bottom: 2rem;
    align-items: inline-block;
    justify-content: space-between;
}

.clearfix:after{
    content: "";
    display: table;
    clear: both;
}
.logo{
    margin-top: -0.2rem;
    padding: 0.45rem 0.8rem;
    background-color: gray;
    width: 12.1rem;
    height: 4.6rem;
    border-radius: 2.5rem;
    text-align: center;
    box-sizing: border-box;
    vertical-align: middle;
}
.t_l{
    color: white;
    font-size: 1.1rem;
}
.header-logo{
    display: flex;
    align-items: center;
    float: left;
    width: auto;
    justify-content: space-between;
    vertical-align: middle;
    padding-left: 13.5rem;
}
.header-contact{
    display: flex;
    width: auto;
    align-items: center;
    float: right;
    padding-right: 23.35rem;
}
.icon_wa{
    margin-top: 0.1rem;
    border-radius: 100%;
    width: 3.45rem;
    height: 3.45rem;

}
.name{
    margin-top: -0.25rem;
    color: white;
    font-size: 1.04rem;
    width: 16.6rem;
    box-sizing: border-box;
    padding: 0 2.7rem;
}
.contacts{
    display: flex;
    align-items: center;
    padding: 0.74rem 0;
}
.schedule{
    color: white;
    font-size: 1.04rem;
    padding: 0 4.9rem;
    margin-top: -0.2rem;
}
.WA{
    margin-top: 0.95rem;
    color: white;
    font-size: 1.05rem;
    text-decoration: underline;
    margin-left: 1rem;
}
</style>