<script>
import { Navigation, Pagination, Autoplay} from 'swiper/modules';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
 export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    data() {
      return {
        modules: [Navigation, Pagination, Autoplay],
        swiperConfig: {
          loop: true,
          speed: 1200,
          navigation: {
            nextEl: '.swiper-button-next',
            prevEl: '.swiper-button-prev',
          },
          autoplay: {
            delay: 5000,
            disableOnInteraction: false,
          },
          breakpoints: { 
            320: {               
              slidesPerView: 1,
              spaceBetween: 10,
            },
            700: {            
              slidesPerView: 2,
              spaceBetween: 50,
            },
            1500: {            
              slidesPerView: 3,
              spaceBetween: 70,
            },
          },
        },
      };
    },  
  }
</script>
<template lang="pug">
  <main>
    .wrapper
      .departure__inner
        .departure
          p оперативный выезд
    .wrapper
      h1.h1 Компьютерный мастер г.&nbspАрхангельск
    section.slider
      swiper.swiper(:modules="modules"
                    v-bind="swiperConfig" )
        .swiper-button-next
          img(src='@/assets/images/arrowRight.svg')
        .swiper-button-prev
          img(src='@/assets/images/arrowLeft.svg')                 
        swiper-slide.slider__item
          img(src='@/assets/images/buildAndChange.png', alt="alt")
          p Сборка, замена комплектующих
        swiper-slide.slider__item
          img(src='@/assets/images/PCbuild.png', alt="alt")
          p Сборка ПК под ключ
        swiper-slide.slider__item
          img(src='@/assets/images/windows.jpg', alt="alt")
          p Установка Windows
        swiper-slide.slider__item
          img(src='@/assets/images/TV1.png', alt="alt")
          p Настройка smartTV
        swiper-slide.slider__item
          img(src='@/assets/images/remont.webp', alt="alt")
          p Ремонт комплектующих
        swiper-slide.slider__item
          img(src='@/assets/images/drivers.jpg', alt="alt")
          p Инсталляция драйверов
    section.sale
      .wrapper
        .sale__inner
          img.leftSale(src='@/assets/images/sale.png')
          h2 СКИДКА НА ПЕРВУЮ ЗАЯВКУ 
          img.rightSale(src='@/assets/images/sale.png')
    section.advantages
      .wrapper
        .advantages__inner
          .advantages__list
            .advantages__item
              img(src='@/assets/images/money.png')
              p Реальная стоимость по телефону
            .advantages__item
              img(src='@/assets/images/money.png')
              p Бесплатный выезд и диагностика
            .advantages__item
              img.master-icon(src='@/assets/images/masterIcon.png')
              p Общаетесь напрямую с мастером. Никаких диспетчеров и посредников.
          .advantages__shiled
            img(src='@/assets/images/shieldIcon.png')
            p Гарантия до 12 мес.
    .wrapper 
      .big-text
        p
          |👨‍🔧Мастер по ремонту пк. 🏃‍♂ Оперативный выезд по всему городу и даже пригороду!<br>
          |✅ Профессиональный ремонт оборудования и техники. Компьютерная помощь. Все заявки выполняю лично! Без посредников и субподрядчиков. По завершении заказа вы получите мой личный контакт для быстрого решения любых вопросов по гарантии. <br>
          | ☎️ Бесплатная предварительная консультация перед началом работ. Не откладывайте решение проблем с оборудованием — звоните прямо сейчас!<br>
        a(href='https://t.me/Dblze_work') 
          img(src='@/assets/images/tg-icon.webp')
          p Написать в телеграмм
    .banner
      .banner__inner
        a.header__tel(href='tel:+79009205567' title='Вызвать мастера')
          img(src='@/assets/images/tel.png')
          h2.header__tel 8 (900) 920-55-67  
    
  </main>
</template>
<style lang="scss" scoped>
@use './Home.scss' as *;
</style>
