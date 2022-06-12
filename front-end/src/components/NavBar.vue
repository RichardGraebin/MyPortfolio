<template>
  <nav class="container">
    <span>GRAEBIN</span>
    <div
      :class="[menuOpen ? 'open' : '', 'menu-btn']"
      @click="changeBtnStatus()"
    >
      <div class="menu-btn__burger"></div>
    </div>
  </nav>
</template>
<style lang="scss">
* {
  font-family: Poppins;
  font-size: 1.5rem;
  color: #fff;
}

nav {
  display: flex;
  justify-content: space-between;
}

span {
  display: flex;
  font-size: 1.75rem;
  align-items: center;
}

.menu-btn {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 80px;
  height: 80px;
  cursor: pointer;

  &__burger,
  &__burger::before,
  &__burger::after {
    content: "";
    position: absolute;
    width: 40px;
    height: 5px;
    background: #fff;
    border-radius: 1px;
    transition: all 0.5s ease-in-out;
  }

  &__burger::before {
    transform: translate(-20px, -13px);
  }
  &__burger::after {
    transform: translate(-20px, 13px);
  }
}

.menu-btn.open .menu-btn__burger {
  transform: translateX(-65px);
  background: transparent;

  &::before {
    transform: rotate(45deg) translate(35px, -35px);
  }

  &::after {
    transform: rotate(-45deg) translate(35px, 35px);
  }
}
</style>
<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";

@Component
export default class NavBar extends Vue {
  private menuBtn = document.querySelector(".menu-btn");
  public menuOpen = false;

  changeBtnStatus() {
    if (!this.menuOpen) {
      this.menuOpen = true;
    } else {
      this.menuOpen = false;
    }
  }
}
</script>
