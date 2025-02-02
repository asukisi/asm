<script setup>
    import { ref } from "vue"
    let flag = ref(true)
    function switcher(){
        flag.value = !flag.value
        console.log(flag.value)
    }
</script>

<template>
    <header :class="flag ? 'light-theme' : 'dark-theme'" class="header">
        <div class="logo">
            <a href="/">
                <img src="./icons/assembly.svg" alt="assembly logo">
                Сайт для изучения ассемблера
            </a>
        </div>
        <nav class="nav">
            <a href="/">Интерактивный учебник</a>
            <a href="/">Форум</a>
        </nav>
        <div class="theme-change">
            <button @click="switcher">
                <img v-if="flag" src="./icons/sun.svg" alt="switch to light theme" width="40px">
                <img v-else src="./icons/moon.svg" alt="switch to dark theme" width="40px">
            </button>
        </div>
    </header>
</template>

<style scoped>
    .header{
        display: flex;
        justify-content: space-between;
        align-items: center;
        row-gap: 5px;
        border-bottom: 2px solid black;
        padding-bottom: 2px;
        padding-top: 2px;
    }

    .nav{
        display: flex;
        gap: 15px;
        
    }
    .nav a{
        background-color: lightgrey;
        padding: 2px;
        border-radius: 10px;
    }

    .logo{
        display: flex;
        align-items: center;
        
    }
    a{
        font-size: 25px;
    }

    .dark-theme {
        background-color: gray;
        color: white;
    }

    .light-theme {
        background-color: white;
        color: black;
}

</style>

