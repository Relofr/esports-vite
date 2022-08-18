<template>
    <div>

        <div class="nav">
            <div class="nav-header">
                <div class="nav-title">
                    <img src="../assets/logo.svg">
                </div>
            </div>
            <div class="nav-btn">
                <label for="nav-check">
                    <span></span>
                    <span></span>
                    <span></span>
                </label>
            </div>

            <div class="nav-links">
                <a href="//github.io/jo_geek" target="_blank">Home</a>
                <a href="http://stackoverflow.com/users/4084003/" target="_blank">Games<fa icon="angle-down"></fa></a>
                <a href="https://in.linkedin.com/in/jonesvinothjoseph" target="_blank">Tournaments<fa icon="angle-down">
                    </fa></a>
                <a href="https://codepen.io/jo_Geek/" target="_blank">Leaderboards</a>
                <a href="https://jsfiddle.net/user/jo_Geek/" target="_blank">
                    <fa icon="user"></fa>
                </a>
                <a href="https://jsfiddle.net/user/jo_Geek/" target="_blank">
                    <fa icon="search"></fa>
                </a>
            </div>
        </div>
        <div class="hero-container">
            <img class="hero-image" src="../assets/images/hero-image.png" alt="">
        </div>
    </div>

</template>

<style lang="less" scoped>
.nav {
    height: 85px;
    width: 100%;
    background-color: var(--secondary-bg-color);
    font-weight: var(--fw-bold);
    position: relative;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 70px;
}

.nav>.nav-header {
    display: inline;
}

.nav>.nav-header>.nav-title {
    display: inline-block;
    color: #fff;
}

.nav>.nav-btn {
    display: none;
}

.nav>.nav-links {
    display: inline;
    float: right;
    font-size: 18px;
}
.fa-angle-down {
    padding-left: 5px;
}

.nav>.nav-links>a {
    display: inline-block;
    padding: 13px 10px 13px 10px;
    text-decoration: none;
    color: #efefef;
}

.nav>.nav-links>a:hover {
    // background-color: rgba(0, 0, 0, 0.3);
}

.nav>#nav-check {
    display: none;
}

@media (max-width:600px) {
    .nav>.nav-btn {
        display: inline-block;
        position: absolute;
        right: 0px;
        top: 0px;
    }

    .nav>.nav-btn>label {
        display: inline-block;
        width: 50px;
        height: 50px;
        padding: 13px;
    }

    .nav>.nav-btn>label:hover,
    .nav #nav-check:checked~.nav-btn>label {
        // background-color: rgba(0, 0, 0, 0.3);
    }

    .nav>.nav-btn>label>span {
        display: block;
        width: 25px;
        height: 10px;
        border-top: 2px solid #eee;
    }

    .nav>.nav-links {
        position: absolute;
        display: block;
        width: 100%;
        background-color: #333;
        height: 0px;
        transition: all 0.3s ease-in;
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
        height: calc(100vh - 50px);
        overflow-y: auto;
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