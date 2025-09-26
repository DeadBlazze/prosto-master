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
</template>

<style lang="scss" scoped>
header{
  background-color: #25274D;
  .header__inner{
    display: flex;
    justify-content: space-between;
    align-items: center;
    p{
      color: white;
      font-family: 'PT Sans';
      font-size: 30px;
      font-weight: 400;
      padding: 20px 0;
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
        padding: 0px 0 20px 0;
      }
      p.header__title{
        font-size: 30px;
        padding: 20px 0 0px 0;
      }
    }
  }
}
</style>
