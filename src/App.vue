<template>
    <NavBar :logo="logo_src" :alt="app_src" />
    <router-view />
    <FooterProject />
</template>

<script>

import NavBar from './components/NavBar.vue'
import FooterProject from './components/FooterProject.vue'

export default {
    name: 'App',
    components: {
        NavBar,
        FooterProject
    },
    data() {
        return {
            logo_src: './img/logo.png',
            app_src: 'Make Your Burguer'
        }
    }
}
</script>
<style>
*{
    font-family: Arial, Helvetica, sans-serif;
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    
}

.min-container{
    margin: 50px;
    min-height: 569px;
}

h1{
    text-align: center;
    font-size: 42px;
    margin-bottom: 30px;
    color: #222;
}
</style>
