<template>
    <div>
        <nav>
            <ul class="menu nav-text">
                <li class="logo"><img src="../assets/logo.svg"></li>
                <li class="item"><a href="#">Home</a></li>
                <li class="item"><a href="#">Games<fa class="fa-icon" icon="angle-down"></fa></a></li>
                <li class="item"><a href="#">Tournaments<fa class="fa-icon" icon="angle-down"></fa></a></li>
                <li class="item"><a href="#">Leaderboards</a></li>
                <li class="item"><a href="#"><fa icon="user"></fa></a></li>
                <li class="item"><a href="#"><fa icon="search"></fa></a></li>

                <li class="toggle"><a href="#">
                        <fa icon="bars"></fa>
                    </a></li>
            </ul>
        </nav>
    </div>
    <div class="hero-container">
        <img class="hero-image" src="../assets/images/hero-image.png" alt="">
    </div>
</template>

<script>
export default {
    mounted() {
        // import('../navbar').then(m => {
        //     return m;
        // });
    },
}
</script>

<style lang="less">
nav {
    background: var(--secondary-bg-color);
    padding: 0 70px;
}

a {
    color: white;
    text-decoration: none;
}

.fa-icon {
    padding-left: 5px;
}

.menu,
.submenu {
    list-style-type: none;
}

.logo img {

    width: 42px;
    height: 42px;
}

li .logo {
    height: 100%;
    align-items: center;
    display: flex;
}

.item {
    padding: 0 15px;
}

/* Mobile menu */
.menu {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    height: 85px;
}

.menu li a {
    display: block;
}

.menu li.subitem a {
    padding: 15px;
}

.toggle {
    order: 1;
    font-size: 20px;
}

.item {
    order: 3;
    width: 100%;
    text-align: center;
    display: none;
}

/* Submenu up from mobile screens */
.submenu {
    display: none;
}

.submenu-active .submenu {
    display: block;
}


.subitem a {
    padding: 10px 15px;
}

.submenu-active {
    background-color: #111;
    border-radius: 3px;
}

/* Tablet menu */
@media all and (min-width: 700px) {
    .menu {
        justify-content: center;
    }

    .logo {
        flex: 1;
    }

    .item.button {
        width: auto;
        order: 1;
        display: block;
    }

    .toggle {
        flex: 1;
        text-align: right;
        order: 2;
    }

    /* Button up from tablet screen */
    .menu li.button a {
        padding: 10px 15px;
        margin: 5px 0;
    }
}

/* Desktop menu */
@media all and (min-width: 960px) {
    .menu {
        align-items: center;
        flex-wrap: nowrap;
        display: flex;
        background: none;
    }

    .logo {
        order: 0;
    }

    .item {
        order: 1;
        position: relative;
        display: block;
        width: auto;
    }

    .submenu-active .submenu {
        display: block;
        position: absolute;
        left: 0;
        top: 68px;
        background: #111;
    }

    .toggle {
        display: none;
    }

    .submenu-active {
        border-radius: 0;
    }
}

.hero-container {
    flex: none;
    order: 0;
    flex-grow: 0;
}

.hero-image {
    height: 325px;
    background-position: center;
    background-repeat: no-repeat;
    position: relative;
    object-fit: cover;

    filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
}
</style>