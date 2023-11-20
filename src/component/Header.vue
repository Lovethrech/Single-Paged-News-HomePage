<script setup>
import { RouterLink } from "vue-router";
import { ref } from "vue";

const showMenu = ref(false);
const menuDisplay = ref("");
const openMenu = () => {
    menuDisplay.value = "block";
    return showMenu.value = false;
}
const closeMenu = () => {
    menuDisplay.value = "none";
    return showMenu.value = true;
}

</script>

<template>
    <div class="container">
        <div class="logo">
            <img src="/public/logo.svg" alt="">
        </div>
        <div class="navbar">
            <RouterLink active-class="is-active" class="navBtn" to="/">Home</RouterLink>
            <RouterLink active-class="is-active" class="navBtn" to="">New</RouterLink>
            <RouterLink active-class="is-active" class="navBtn" to="">Popular</RouterLink>
            <RouterLink active-class="is-active" class="navBtn" to="">Trending</RouterLink>
            <RouterLink active-class="is-active" class="navBtn" to="">Categories</RouterLink>
        </div>
        <div class="menubar">
            <i v-if="showMenu" @click="openMenu()" class='bx bx-menu'></i>
            <i v-else  class='bx bx-x' @click="closeMenu()"></i>
        </div>
    </div>
    <div class="contain-menu">
        <div class="menu" :style="{display:menuDisplay}">
            <RouterLink class="navBtn" to="/">Home</RouterLink>
            <RouterLink class="navBtn" to="/new">New</RouterLink>
            <RouterLink class="navBtn" to="/popular">Popular</RouterLink>
            <RouterLink class="navBtn" to="/trend">Trending</RouterLink>
            <RouterLink class="navBtn" to="/categories">Categories</RouterLink>
        </div> 
    </div>

</template>
<style scoped>
.container{
    display:flex;
    justify-content: space-between;
}
.logo img{
    width: 50px;
}
.navbar .navBtn{
    text-decoration:none;
    margin:0 10px;
    color: hsl(0, 0%, 0%);
    font-weight:500;
}
.menubar{
    font-size:30px;
    color:hsl(0, 0%, 0%);
    display:none;
}

.menu{
    position:absolute;
    top:0;
    right:0;
    background-color: hsl(0, 100%, 100%);
    display:none;
    transition: all .72s;
}
.menu .navBtn{
    text-decoration:none;
    margin:0 10px;
    color: hsl(0, 0%, 0%);
    font-weight:500;
    display: block;
}

@media screen and (max-width:650px){
    .navbar{
        display:none;
    }
    .menubar{
        display:block;
        margin:auto 0;
    }
    .menu{
        top:80px;
        display:block;
        width:200px;
        height:60vh;
        padding:20px;
    }
    .menu .navBtn{
        margin: 20px 0;
    }
}

</style>