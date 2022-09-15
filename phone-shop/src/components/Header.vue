<template>
    <header class="header">
        <div class="container">
            <!--<div class="nav-panel">
                <h3 class="title">{{title}}</h3>
                <div class="sections">
                    <ul class="sections-list">
                        <li class="section"> <a href="#" class="section-link">Главная</a></li>
                        <li class="section"> <a href="#" class="section-link">Каталог</a></li>
                        <li class="section"> <a href="#" class="section-link">Отзывы</a></li>
                        <li class="section"> <a href="#" class="section-link">Контакты</a></li>
                        <li class="section"> <a href="#" class="section-link">О нас</a></li>
                    </ul>
                </div>
            </div>-->
            <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
                <div class="container-fluid">
                    <a class="navbar-brand" href="#">Shop</a>
                    <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
                        data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent"
                        aria-expanded="false" aria-label="Переключатель навигации">
                        <span class="navbar-toggler-icon"></span>
                    </button>
                    <div class="collapse navbar-collapse" id="navbarSupportedContent">
                        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                            <li class="nav-item">
                                <a class="nav-link active" aria-current="page" href="#">Главная</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="#">Каталог</a>
                            </li>
                            <li class="nav-item dropdown">
                                <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                                    data-bs-toggle="dropdown" aria-expanded="false" @click="openMenu">
                                    Категории
                                </a>
                                <ul v-show="isOpen" class="dropdown-menu" aria-labelledby="navbarDropdown">
                                    <li><a class="dropdown-item" href="#">Iphone</a></li>
                                    <li><a class="dropdown-item" href="#">Ipad</a></li>
                                    <li><a class="dropdown-item" href="#">Аксесуары</a></li>
                                    <li><a class="dropdown-item" href="#">Ремонт</a></li>
                                    <li>
                                        <hr class="dropdown-divider">
                                    </li>
                                    <li><a class="dropdown-item" href="#">Подарки</a></li>
                                </ul>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link disabled">Отключенная</a>
                            </li>
                        </ul>
                        <form class="d-flex">
                            <input class="form-control me-2" type="search" placeholder="Поиск" aria-label="Поиск">
                            <button class="btn btn-outline-success" type="submit">Поиск</button>
                        </form>
                    </div>
                </div>
            </nav>
        </div>
    </header>
</template>
<script>
export default {
    name: 'Header',
    data() {
        return {
            isOpen: false,
            navDropdownMenu: 'navDropdownMenu'
        }
    },
    props: {
        title: String
    },
    methods: {
        openMenu() {
            this.isOpen = !this.isOpen;
        }
    }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less" >
@font-face {
    font-family: 'Montserrat-Bold';
    src: url('../assets/fonts/Montserrat-ExtraBold.ttf');
}

@font-face {
    font-family: 'Montserrat-Regular';
    src: url('../assets/fonts/Montserrat-Regular.ttf');
}

@container: 1440px;
@centre: 0 auto;
@bgc: rgba(33, 37, 41);

* {
    margin: 0;
    padding: 0;
}

.width-old-tag {
    width: 100%;
    max-width: 1920px;
}

.header {
    background-color: @bgc;
    .width-old-tag();
    justify-content: center;
}

.container {
    width: @container;
    margin: @centre;
    display: flex;
    flex-direction: column;
    /*position: relative;*/
}

.nav-panel {
    /*position: absolute;
    top: 50%;*/
    display: flex;
    align-items: center;
}

.dropdown-menu {
    display: block;
}

.title {
    font-family: 'Montserrat-Bold';
    letter-spacing: .12em;
    color: #fff;
}

.sections {
    margin: @centre;
    min-width: 500px;
}

.sections-list {
    display: flex;
    list-style: none;
    justify-content: space-around;
}

.section-link {
    text-decoration: none;
    .title();
    font-family: 'Montserrat-Regular';
}
</style>