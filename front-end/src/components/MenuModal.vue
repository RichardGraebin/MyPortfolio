<template>
  <div class="menu-container">
    <div class="menu__">
      <ul>
        <li>Home</li>
        <li>About</li>
        <li>What i know</li>
        <li>Contact</li>
        <li>More</li>
      </ul>
    </div>
  </div>
</template>
<style lang="scss">
.menu-container {
  position: fixed;
  background: red;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;

  .menu__ {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>
<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";

@Component
export default class MenuModal extends Vue {}
</script>
