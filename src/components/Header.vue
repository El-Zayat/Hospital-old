<template>
  <header class="Header">
    <div class="theContent">
      <h1>مرحبا بكم في دار الطب</h1>
      <p>مستشفي دار الطب بالمنصورة من ضمن مشروع أندلسية المكون ايضا من حي سكني و مول تجاري</p>
      <v-btn outlined color="white" class="btn d-block mx-auto mb-5" height="50px" width="150px">شارك الآن</v-btn>
      <a class="btn trigger" text>
        <v-icon class="white--text angle">fa fa-angle-double-down</v-icon>
      </a>
    </div>
  </header>
</template>

<script>
import $ from 'jquery'

export default {
  mounted() {
    $(".trigger").click(function() {
      $([document.documentElement, document.body]).animate({
          scrollTop: $("#content").offset().top - 130
      }, 1000);
    });
  }
}
</script>

<style lang="scss">
@import '../assets/style/config';

.Navbar header{
  background: transparent !important;

  &.v-app-bar--is-scrolled {
    background: rgba(34, 34, 34, 0.85) !important;
  }
}

.Header {
  position: relative;
  top: 0;
  width: 100%;
  height: calc(100vh + 70px);
  background-image: url('../assets/img/banner.jpg');
  background-size: cover;
  
  &::after {
    content: '';
    background: rgba(0, 108, 255, 0.7);
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
  }

  .theContent {
    position: absolute;
    top: 54%;
    left: 50%;
    color: #FFF;
    transform: translate(-50%, -50%);
    text-align: center;
    user-select: none;
    z-index: 5;

    h1 {
      font-size: 4em;
    }

    p {
      font-size: 1.8em;
      margin-top: 20px;
    }
    
    .btn {
      margin-top: 50px;
      font-size: 1.1em;
    }

    .angle {
      padding-top: 60px;
    }
  }
}
</style>