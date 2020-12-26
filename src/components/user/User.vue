<template>
  <div>
    <h1>The User Page</h1>
    <hr />
    <button class="btn btn-primary" @click="navigateHome">Go Home</button>
    <hr />
    <transition name="slide" mode="out-in">
      <router-view></router-view>
    </transition>
  </div>
</template>

<script>
export default {
  methods: {
    navigateHome() {
      this.$router.push({ name: "home" });
    },
  },
};
</script>

<style>
.slide-enter-active,
.slide-leave-active {
  transition: opacity 0.6s;
}
.slide-enter,
.slide-leave-to {
  opacity: 0;
}
</style>
