<script>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template lang="pug">
  header.header
    .wrapper
      nav.header__inner
        a(href='#') 
          p.header__title просто-мастер.рф
        a.header__tel(href='tel:+79009205567')
          p.header__tel(title='Вызвать мастера') 8 (900) 920-55-67
  RouterView
  footer.footer
    .wrapper
      p ИНН 292303316874
      .footer__copyright
        p просто-мастер.рф
        img(src='@/assets/images/copyright2.svg')
        p 2025
      p Батраков Игорь Николаевич
</template>

<style lang="scss" scoped>
header{
  background-color: #25274D;
  padding: 20px 0;
  .header__inner{
    display: flex;
    justify-content: space-between;
    align-items: center;
    p{
      color: white;
      font-family: 'PT Sans';
      font-size: 30px;
      font-weight: 400;
    }
    p.header__title{
      font-size: 35px;
    }
    p.header__tel{
      top: 4px;
    }
    @media (max-width: 660px){
      p{
        font-size: 25px;
        position: relative;        
      }
      // a.header__tel{
        //   align-self: flex-end;
        // }
        p.header__tel{
          top: 3px;
        }
        p.header__title{
          font-size: 30px;
        }
      }
      @media (max-width: 560px){
        flex-direction: column;
        align-items: flex-start;
        justify-content:flex-start;
        p{
          font-size: 25px;
          position: relative;
        }
        p.header__tel{
          top: 3px;
          padding: 0;
        }
        p.header__title{
          font-size: 30px;
          padding: 0;
        }
      }
    }
  }
  footer{
    background-color: #25274D;
    padding: 30px 0 25px 0;
    gap: 10px;
    display: flex;
    flex-direction: column;
    font-size: 25px;
    font-family: 'PT Sans';
    color: white;
    @media(max-width:700px){
      font-size: 20px;
    }
    img{
      width: 27px;
      object-fit: contain;
      @media(max-width:700px){
        width: 21px;
      }
    }
    .footer__copyright{
      display: flex;
      gap: 5px;
      align-items: center;
      p{
        position: relative;
        top: -2px;
      }
    }
}
</style>
