<template>
  <header class="header">
    <div class="header__top">
        <div class="container">
            <div class="header__top-head">
                <img src="./assets/img/logo.svg" alt="" class="header__top-head-logo">
                    <nav class="header__top-head-nav">
                        <a href="#tours" class="header__top-head-nav_a">Туры</a>
                        <a href="" class="header__top-head-nav_a">Отели</a>
                        <a href="" class="header__top-head-nav_a">Достопримечательности</a>
                    </nav>
                <img src="./assets/img/cart.svg" alt="" class="header__top-head-cart">
            </div>
          </div>
      </div>
    <div class="header__bottom">
        <div class="container">
            <div class="content-center">
                <div class="header__bottom-content">
                    <h1 class="header__bottom-content-slogan">Открой для себя<br>прекрасную ЯПОНИЮ</h1>
                    <p class="header__bottom-content-lozung">Найди свое вдохновенье здесь!</p>
                    <button class="btn header__bottom-content-btn">Посмотреть</button>
                </div>
            </div>
        </div>       
    </div>
  </header>

  <section class="slider">
      <carousel :items-to-show="1" :autoplay="5000" :transition="1500" :wrap-around="true" :touchDrag="false" :mouseDrag="false">
        <slide v-for="(item, index) in sliderArray" :key="index">
            <div class="slider__container">
                <img :src="require(`./assets/img/forSlider/${item.img}`)" alt="" class="slider__container-img">
                <div class="slider__container-content">
                    <h2 class="slider__container-content-slogan">{{item.h2}}</h2>
                    <p class="slider__container-content-information">{{item.inf}}</p>
                </div>
            </div>
        </slide>       
    </carousel>
  </section>

  <section class="tours" id="tours">
    <div class="container">
        <div class="tours-nav">
            <div class="tours-sectiont-slash"></div>
            <h3 class="tours-sectiont-name">Туры</h3>
        </div>
        <div class="tour">
            <img src="./assets/img/forTours/tour1.jpg" alt="" class="tour-img">
            <div class = "tour-product">
                <div class="tour-name-and-inf">
                    <h3 class="tour-name">Классическая Япония 8 дней/7 ночей</h3>
                    <p class="tour-inf">В программу тура по Японии "Классическая Япония" входит проживание в Токио, Киото и 4 экскурсии с русскоговорящим гидом, во время которых мы предлагаем вам посетить Токио - современную столицу Японии, курортную зону Фудзи-Хаконе и древние столицы Японии Киото и Нара.</p>
                </div>
                <button class = "btn tour-btn">добавить</button>
            </div>
        </div>
        <div class="tour">
            <img src="./assets/img/forTours/tour2.jpg" alt="" class="tour-img">
            <div class = "tour-product">
                <div class="tour-name-and-inf">
                    <h3 class="tour-name">Транзитный тур в Японию Токио транзитом 1 день</h3>
                    <p class="tour-inf">Токио - столица Японии, один из крупных городов мира наряду с Нью-Йорком, Парижем и Лондоном. Токио обладает пленительным очарованием, в нем переплетаются авангард настоящего времени и традиционная культура периода Эдо.</p>
                </div>
                <button class = "btn tour-btn">добавить</button>
            </div>
        </div>
        <div class="tour">
            <img src="./assets/img/forTours/tour3.jpg" alt="" class="tour-img">
            <div class = "tour-product">
                <div class="tour-name-and-inf">
                    <h3 class="tour-name">Экскурсия в первую столицу сегунов Камакура</h3>
                    <p class="tour-inf">Сегодня мы с вами отправляемся на полуостров Миура в древнюю столицу Японии Камакура. Этот небольшой городок раскинулся на берегу живописного залива Сагами. Мы познакомимся с культурой самураев периода Камакура, характерной чертой которой является реальными...</p>
                </div>
                <button class = "btn tour-btn">добавить</button>
            </div>
        </div>



    </div>
  </section>
</template>

<script>
import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide } from 'vue3-carousel';
export default {
    data() {
        return {
            sliderArray: [
                {id: 1, img: "Slide1.svg", h2: "Прекрасный гид!", inf: "Незабываемые экскурсии по красочной Японии и знакомства с новыми людьми! Вы посетите все значимые места самурайского мира."},
                {id: 2, img: "Slide2.svg", h2: "Отличные цены!", inf: "Мы всегда стараемся обеспечить лучшее качество за небольшую плату"},
                {id: 3, img: "Slide3.svg", h2: "Шикарные виды!", inf: "Вы посетите лучшие места Японии и сделаете ЛУЧШУЮ фотосессию в вашей жизни"}
            ]
        }
    },

    components: {
        Carousel,
        Slide,
    },
}
</script>

<style scoped>
    @import url(./assets/styles/header.css);
    @import url(./assets/styles/slider.css);
    @import url(./assets/styles/tours.css);
 

</style>
