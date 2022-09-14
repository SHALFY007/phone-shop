<template>
    <header class="header">
        <div class="container">
            <div class="nav-panel">
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
            </div>
        </div>
    </header>
</template>
<script>
export default {
    name: 'Header',
    props: {
        title: String
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
@header-height: 65px;
@centre: 0 auto;
@bgc: #2c3e50;

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
    min-height: @header-height;
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
    min-height: @header-height;
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