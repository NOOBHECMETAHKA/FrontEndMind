<template>
  <header class="header">
    <div class="container">
      <div class="header__inner">
        <a href="" class="logo">
          <logo-icon-site></logo-icon-site>
        </a>
        <nav class="menu">
          <button class="menu_btn" @click="showMenu()">
            <menu-icon-site></menu-icon-site>
          </button>
          <ul class="menu__list" :class="{'menu__list--open': isActive}">
            <li class="menu__close" @click="closeMenu()">
              <close-icon-site></close-icon-site>
            </li>
            <li class="menu__item">
              <a href="" class="menu__link">Black</a>
            </li>
            <li class="menu__item">
              <a href="" class="menu__link">Green</a>
            </li>
            <li class="menu__item">
              <a href="" class="menu__link">White</a>
            </li>
            <li class="menu__item">
              <a href="" class="menu__link">OOlong</a>
            </li>
            <li class="menu__item">
              <a href="" class="menu__link">Pu-erh</a>
            </li>
            <li class="mobile-nav">
              <ul class="mobile-menu">
                <li class="mobile-menu__item">
                  <a href="#" class="mobile__menu-link">Contact us</a>
                </li>
                <li class="mobile-menu__item">
                  <a href="#" class="mobile__menu-link">Our Blog</a>
                </li>
                <li class="mobile-menu__item">
                  <a href="#" class="mobile__menu-link">Shipping and Delivery</a>
                </li>
              </ul>
              <ul class="mobile-actions">
                <li class="mobile-actions__item">
                  <a href="#" class="mobile-actions__link">
                    <basket-icon-site></basket-icon-site>
                  </a>
                </li>
                <li class="mobile-actions__item">
                  <a href="#" class="mobile-actions__link">
                    <user-icon-site></user-icon-site>
                  </a>
                </li>
                <li class="mobile-actions__item">
                  <a href="#" class="mobile-actions__link">
                    <search-icon-site></search-icon-site>
                  </a>
                </li>
              </ul>
            </li>
          </ul>
        </nav>
        <ul class="user-actions">
          <li class="user-actions__item">
            <a href="#" class="user-actions__link">
              <basket-icon-site></basket-icon-site>
            </a>
          </li>
          <li class="user-actions__item">
            <a href="#" class="user-actions__link">
              <user-icon-site></user-icon-site>
            </a>
          </li>
          <li class="user-actions__item user-actions__item-search">
            <a href="#" class="user-actions__link">
              <search-icon-site></search-icon-site>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </header>

  <main class="main">
    <section class="top">
      <div class="container">
        <div class="top__inner">
          <h1 class="top__title">
            A cup of tea is a moment of calm in the chaos of life
          </h1>
          <p class="top__text">
            Wide selection of high-quality teas from all over the world, carefully curated by tea experts.
          </p>
        </div>
      </div>
    </section>
    <blockquote class="blockquote">
      <p class="blockquote__text">
        "Tea is not just a drink, it's a way of life and a way to connect with our loved ones."
      </p>
    </blockquote>
  </main>
</template>

<script>
import LogoIconSite from "@/components/svg/LogoIconSite.vue";
import BasketIconSite from "@/components/svg/BasketIconSite.vue";
import UserIconSite from "@/components/svg/UserIconSite.vue";
import SearchIconSite from "@/components/svg/SearchIconSite.vue";
import MenuIconSite from "@/components/svg/MenuIconSite.vue";
import CloseIconSite from "@/components/svg/CloseIconSite.vue";
export default {
  data() {
    return {
      isActive: false,
    };
  },
  components: {
    LogoIconSite,
    BasketIconSite,
    UserIconSite,
    SearchIconSite,
    MenuIconSite,
    CloseIconSite
  },
  methods: {
    showMenu(){
      this.isActive = !this.isActive;
    },
    closeMenu(){
      this.isActive = false;
    }
  }
}
</script>