<template>
    <main class="main">
        <aside class="aside">
           
                <a href="/">Раздел 1</a>
                <a href="/">Раздел 2</a>
                <a href="/">Раздел 3</a>
           
        </aside>
        <article>
             <slot></slot>
        </article>
    </main>
</template>

<style scoped> 
    
    .main{
        display:flex;
    }
    .aside{
        display: flex;
        flex-direction: column;
        padding: 1px;
        width: 10%;
        border-right: 2px solid black;
        font-size: 25px;
    }
    .aside a{
        background-color: lightgrey;
        padding: 2px;
        border-radius: 10px;
    }
    article{
        width: 80%;
    }
</style>