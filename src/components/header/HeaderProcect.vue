<script setup>
document.addEventListener('DOMContentLoaded', () => {
    const searchInput = document.querySelector('.search-header__input');
    const searchRemoveButton = document.querySelector('.search-header__remove');

    searchInput.addEventListener('input', () => {
        if (searchInput.value.length > 0) {
            searchRemoveButton.classList.add('--active');
        } else {
            searchRemoveButton.classList.remove('--active');
        }
    });

    searchRemoveButton.addEventListener('click', () => {
        searchInput.value = '';
        searchRemoveButton.classList.remove('--active');
        searchRemoveButton.classList.add('--hidden');
    });
});
</script>

<template>
    <header class="header">
        <div class="header__logo logo-header">
            <div class="logo-header__img">
                <img src="../../img/header/img-none.png" alt="">
            </div>
            <span class="logo-header__txt">Логотип</span>
        </div>
        <a href="#" class="header__catalog catalog-header">
            <div class="catalog-header__txt">Каталог</div>
        </a>
        <div class="header__search search-header">
            <button class="search-header__back">
                <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path opacity="0.3" fill-rule="evenodd" clip-rule="evenodd"
                        d="M0.283445 10.6843C-0.0944816 10.3064 -0.0944816 9.69363 0.283445 9.3157L9.3157 0.283445C9.69363 -0.0944804 10.3064 -0.0944804 10.6843 0.283445C11.0622 0.661371 11.0622 1.27411 10.6843 1.65204L3.30408 9.03226L19.0323 9.03226C19.5667 9.03226 20 9.46553 20 10C20 10.5345 19.5667 10.9677 19.0323 10.9677L3.30408 10.9677L10.6843 18.348C11.0622 18.7259 11.0622 19.3386 10.6843 19.7166C10.3064 20.0945 9.69363 20.0945 9.3157 19.7166L0.283445 10.6843Z"
                        fill="#333333" />
                </svg>
            </button>
            <input class="search-header__input" type="text" placeholder="Поиск по 100 000 товаров">
            <button class="search-header__remove">
                <svg class="remove" width="18" height="18" viewBox="0 0 18 18" fill="none"
                    xmlns="http://www.w3.org/2000/svg">
                    <path fill-rule="evenodd" clip-rule="evenodd"
                        d="M17.3334 9.00001C17.3334 13.6024 13.6025 17.3333 9.00008 17.3333C4.39771 17.3333 0.666748 13.6024 0.666748 9.00001C0.666748 4.39764 4.39771 0.666679 9.00008 0.666679C13.6025 0.666679 17.3334 4.39764 17.3334 9.00001ZM12.0893 7.08927C12.4148 6.76383 12.4148 6.23619 12.0893 5.91076C11.7639 5.58532 11.2363 5.58532 10.9108 5.91076L9.00008 7.8215L7.08934 5.91076C6.7639 5.58532 6.23626 5.58532 5.91083 5.91076C5.58539 6.23619 5.58539 6.76383 5.91083 7.08927L7.82157 9.00001L5.91083 10.9108C5.58539 11.2362 5.58539 11.7638 5.91083 12.0893C6.23626 12.4147 6.7639 12.4147 7.08934 12.0893L9.00008 10.1785L10.9108 12.0893C11.2363 12.4147 11.7639 12.4147 12.0893 12.0893C12.4148 11.7638 12.4148 11.2362 12.0893 10.9108L10.1786 9.00001L12.0893 7.08927Z" />
                </svg>
            </button>
            <button class="search-header__btn">Найти</button>
        </div>
        <ul class="header__menu menu-header">
            <li><a class="menu-header__item" href="#">Информация о компании</a></li>
            <li><a class="menu-header__item" href="#">Контакты</a></li>
            <li><a class="menu-header__item" href="#">Полезные ссылки</a></li>
        </ul>
    </header>
</template>

<style lang="scss" scoped src="./HeaderProject.scss"/>