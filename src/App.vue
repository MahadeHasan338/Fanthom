<template>
  <div class="flex body-background">
    <header class="absolute lg:static top-0 w-[19rem] z-[99]">
      <the-navigation></the-navigation>
    </header>

    <main class="w-full overflow-y-auto">
      <the-header @show-the-modal="showWalletModal = true"></the-header>
      <div class="z-[999]">
        <ConnectWalletModal v-show="showWalletModal" @close-modal="showWalletModal = false" />
        
      </div>
      <transition name="scale" mode="out-in">
        <router-view @show-the-modal="showWalletModal = true"></router-view>
      </transition>
    </main>
  </div>
</template>

<script>
import TheNavigation from "./components/common/TheNavigation.vue";
import TheHeader from "./components/common/TheHeader.vue";
import ConnectWalletModal from "./components/modal/ConnectWalletModal.vue";

export default {
  data() {
    return {
      showWalletModal: false,
    };
  },
  components: {
    TheNavigation,
    TheHeader,
    ConnectWalletModal,
  },
};
</script>
<style>
.apexcharts-tooltip {
  background-color: rgba(60, 67, 78, 0.99) !important;
  color: white;
  border-color: rgba(60, 67, 78, 0.99) !important;
  width: 300px;
  border-radius: 20px !important;
  padding: 8px 20px;
}

.apexcharts-tooltip-title {
  background-color: rgba(60, 67, 78, 0.99) !important;
  color: white;
  border-color: rgba(60, 67, 78, 0.99) !important;
}
.body-background {
  @apply h-full w-full;
  background: linear-gradient(180deg, #313945, #161d26) no-repeat;
  position: fixed;
}
.scale-enter-active,
.scale-leave-active {
  transition: all 0.2s ease;
}

.scale-enter-from,
.scale-leave-to {
  opacity: 0;
  transform: scale(0.2);
}
</style>
