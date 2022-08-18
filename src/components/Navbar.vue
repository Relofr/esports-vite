<template>
    <div class="nav">
        <input type="checkbox" id="nav-check">
        <div class="nav-header">
            <img class="logo" src="../assets/logo.svg">
        </div>
        <div class="nav-btn">
            <label for="nav-check">
                <fa icon="burger" size="2xl"></fa>
            </label>
        </div>

        <div class="nav-links">
            <a href="#" target="_blank">Home</a>
            <a href="#" target="_blank">Games<fa class="down-arrow" icon="caret-down"/></a>
            <a href="#" target="_blank">Tournaments<fa class="down-arrow" icon="caret-down"/></a>
            <a href="#" target="_blank">Leaderboards</a>
            <a href="#" target="_blank">
                <fa icon="user"></fa>
            </a>
            <a href="#" target="_blank">
                <fa icon="search"></fa>
            </a>
        </div>
    </div>
    <div class="hero-container">
        <img class="hero-image" src="../assets/images/hero-image.jpeg" alt="">
    </div>
</template>

<script>

</script>

<style>
.logo {
    width: 42px;
    height: 42px;
}

.nav {
    height: 65px;
    width: 100%;
    padding: 0 70px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: var(--secondary-bg-color);
}

.down-arrow {
    padding-left: 10px;
}

.nav>.nav-header>.nav-title {
    display: inline-block;
    font-size: 22px;
    color: #fff;
    padding: 10px 10px 10px 10px;
}

.nav>.nav-btn {
    display: none;
}

.nav>.nav-links {
    display: inline;
    float: right;
    font-size: 18px;
    font-weight: var(--fw-bold);
}

.nav>.nav-links>a {
    display: inline-block;
    padding: 13px 10px 13px 10px;
    text-decoration: none;
    color: #efefef;
}

.nav svg:hover {
    cursor: pointer;
    /* background-color: rgba(0, 0, 0, 0.3); */
}

.nav>#nav-check {
    display: none;
}

@media (max-width:800px) {
    .nav {
        padding: 15px;
    }

    svg {
        color: white;
    }

    .nav>.nav-btn {
        display: flex;
        width: 100%;
        justify-content: flex-end;
    }

    .nav>.nav-links {
        position: absolute;
        display: block;
        width: 100%;
        background-color: var(--secondary-bg-color);
        height: 0px;
        transition: all 0.3s ease-in;
        padding: 0 15px;
        overflow-y: hidden;
        top: 50px;
        left: 0px;
    }

    .nav>.nav-links>a {
        display: block;
        width: 100%;
    }

    .nav>#nav-check:not(:checked)~.nav-links {
        height: 0px;
    }

    .nav>#nav-check:checked~.nav-links {
        height: auto;
        overflow-y: auto;
    }
}
</style>