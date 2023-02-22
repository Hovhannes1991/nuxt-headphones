<template>
    <nav class="nav">
        <div class="left">
            <div class="img_wrapper">
                <img src="icons/logo.svg" alt="Logo icon">
            </div>
        </div>
        <div class="center">
            <div class="img_wrapper flex-center">
                <img src="icons/search.svg" alt="search icon">
            </div>
            <div class="line"></div>
            <div class="img_wrapper flex-center">
                <img src="icons/mail.svg" alt="mail icon">
            </div>
            <div class="line"></div>
            <div class="img_wrapper flex-center">
                <img src="icons/user.svg" alt="user icon">
            </div>

        </div>
        <div class="right">
            <div class="img_wrapper">
                <img src="icons/burger-menu.svg" alt="burger menu icon">
            </div>
        </div>
    </nav>
</template>

<style lang="scss" scoped>
nav {
    display: flex;
    margin: 0 auto;
    align-items: center;
    justify-content: space-around;

    .center {
        display: flex;
        gap: 30px;

        .img_wrapper {
            height: 50px;
            width: 50px;
            background-color: #fff;
            border-radius: 100%;
        }

        .line {
            width: 1px;
            height: 50px;
            background: #fff;
            opacity: 0.5;
        }
    }

    .center,
    .right {
        .img_wrapper {
            cursor: pointer;
        }
    }
}
</style> 