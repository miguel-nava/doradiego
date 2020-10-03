<template>
    <div v-bind:class="{ 'hamburger': !showMenu, 'close': showMenu, 'icon': true}" @click="showMenu = !showMenu">
        <div></div>
    </div>
    <nav v-bind:class="{ 'active': showMenu }">
        <ul>
            <li><a href="#diego" @click="showMenu = !showMenu">Diego</a></li>
            <li class="divider"></li>
            <li><a href="#dora" @click="showMenu = !showMenu">Dora</a></li>
        </ul>
    </nav>
</template>

<script>
import { Vue } from 'vue-class-component';

export default class NavBar extends Vue {
    showMenu = false;

    toggleMenu() {
        console.log(this.showMenu)
    }

}
</script>

<style scoped lang="scss">
.icon {
    width: 50px;
    height: 50px;
    position: relative;
    z-index: 3;
    margin: .5em 1em 0;
    div {
        position: absolute;
        width: 50px;
        height: 2px;
        background: black;
        top: 25px;
    }
}
.icon:hover {
    cursor: pointer;
}
.close {
    position: sticky;

    div {
        transform: rotate(45deg);
    }
    div::before {
        content: '';
        position: absolute;
        height: 50px;
        width: 2px;
        background: black;
        top: -25px;
        left: 25px;
    }
}
.hamburger {
    
    div::before {
        content: '';
        position: absolute;
        width: 50px;
        height: 2px;
        background: black;
        top: -10px;
        left: 0;
    }
    div::after {
        content: '';
        position: absolute;
        width: 50px;
        height: 2px;
        background: black;
        top: 10px;
        left: 0;
    }
}

.active {
    transform: translateX(0);
}

nav {
    position: fixed;
    top: 0;
    transform: translateX(-100%);
    transition: transform 150ms ease-in;
    z-index: 2;
}

ul {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    list-style: none;
    background: whitesmoke;
    font-size: 5rem;
    width: 100vw;
    height: 100vh;

    li {
        align-self: center;
    }
}

.divider {
    align-self: center;
    width: 40%;
    height: 2px;
    background: rgba(0,0,0,.3);
}

a {
    text-decoration: none;
}
</style>