<template>
  <nav class="Navbar">
    <v-app-bar class="white--text" fixed elevation="0" elevate-on-scroll height="60px">
      <v-toolbar-title class="brand">
        <router-link to='/' class="white--text">
          <v-icon class="white--text ml-3">fa fa-hospital-o</v-icon>
          دار الطب بالمنصورة
        </router-link>
      </v-toolbar-title>
      <v-list class="links transparent">
        <v-list-item class="item">
          <router-link to="/">
            <v-icon>fa fa-home</v-icon>
            الرئيسية
          </router-link>
        </v-list-item>
        <v-list-item class="item">
          <router-link to="/services">
            <v-icon>fa fa-gear</v-icon>
            خدماتنا    
          </router-link>
        </v-list-item>
        <v-list-item class="item">
          <router-link to="/about">
            <v-icon>fa fa-users</v-icon>
            من نحن
          </router-link>
        </v-list-item>
        <v-list-item class="item">
          <router-link to="/contact">
            <v-icon>fa fa-phone</v-icon>
            تواصل معنا
          </router-link>
        </v-list-item>
      </v-list>
      <a class="fb" href="https://www.facebook.com/Eskan.mansourafirst">
        <v-icon>fa fa-facebook-square</v-icon>
      </a>
    </v-app-bar>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          title: 'الرئيسية',
          link: '/',
          icon: ''
        }
      ]  
    }
  },
}
</script>

<style lang="scss">
@import '../assets/style/config';

.Navbar {
  z-index: 10;

  header {
    background: rgba(34, 34, 34, 0.85) !important;
  }

  .brand {
    margin-right: 100px;
  }

  .links {
    margin: auto;
    padding: 0;
    display: flex;
    
    .item {
      min-width: 150px;
      text-align: center;

      a {
        color: #FFF !important;
        transition: .3s;

        &:hover {
          color: #d8cece !important;

          i {
            color: #d8cece !important;
          }
        }

        &:active {
          transform: translateY(1px);
        }

        i {
          color: #FFF;
          font-size: 16px;
          margin-left: 5px;
        }
      }
    }
  }

  .fb {
    margin-left: 100px;
    transition: .3s;
    
    i {
      color: #FFF !important;

      &:hover {
        color: #ddd !important;
      }
    }

  }
}
</style>