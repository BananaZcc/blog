<template>
  <div class="layout full-height">
    <div class="aside-nav full-height">
      <Navbar />
    </div>
    <div class="main-body full-height">
      <transition name="fade" mode="out-in">
        <keep-alive>
          <router-view />
        </keep-alive>
      </transition>
    </div>
  </div>
</template>

<script>
import Navbar from './navbar.vue';

export default {
  name: 'layout',
  components: {
    Navbar
  }
};
</script>

<style lang="scss" scoped>
@import '~@/styles/common-variables';
.layout {
  .aside-nav {
    position: fixed;
    top: 0;
    left: 0;
    bottom: 0;
  }
  .main-body {
    width: 100%;
    height: 100%;
  }
}
</style>
