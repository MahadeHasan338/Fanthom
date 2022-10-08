<template>
  <transition name="modal-fade">
    <div
      class="
        fixed
        top-0
        bottom-0
        right-0
        left-0
        z-[999]
        flex
        justify-center
        items-center
        background-overlay
      "
      @click="$emit('close-modal')"
    >
      <!-- Modal body -->
      <div class="text-center bg-white rounded-2xl" @click.stop>
        <div class="grid grid-cols-1 justify-center items-center  ">
          <div class="p-2 sm:p-3">
            <div
            class="
              py-4
              sm:py-6
              px-5
              sm:px-16
              hover:bg-[#F3F3F3]
              transition-all
              duration-300
              rounded-2xl
            "
          >
            <img
              class="w-10 mb-2 inline"
              src="../../assets/icon/modal/fox.svg"
              alt=""
            />
            <h3 class="text-2xl font-extrabold text-[#0C0C0D]">MetaMask</h3>
            <p class="text-[#A9A9BC] text-md sm:text-lg -mt-1">
              Connect to your MetaMask Wallet
            </p>
          </div>
          </div>

          <span class="block w-full h-[1px] bg-slate-200"></span>

          <div class="p-2 sm:p-3">
            <div
            class="
              py-4
              sm:py-6
              px-5
              sm:px-16
              hover:bg-[#F3F3F3]
              transition-all
              duration-300
              rounded-2xl
            "
            @click="showModal = true"
          >
            <img
              class="w-10 mb-2 inline"
              src="../../assets/icon/modal/wallet-2.svg"
              alt=""
            />
            <h3 class="text-2xl font-extrabold text-[#0C0C0D]">
              WalletConnect
            </h3>
            <p class="text-[#A9A9BC] text-md sm:text-lg -mt-1">
              Scan with WalletConnect to connect
            </p>
          </div>
          </div>
          <!-- Modal -->
          <Modal v-show="showModal" @close-modal="showModal = false" />
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
import Modal from "./TheModal.vue";
export default {
  emits: ["close-modal"],
  components: {
    Modal,
  },
  data() {
    return {
      checked: true,
      showModal: false,
    };
  },
};
</script>

<style scoped>
.modal-fade-enter-from,
.modal-fade-leave-to {
  opacity: 0;
}
.modal-fade-enter-active,
.modal-fade-leave-active {
  transition: opacity 0.5s ease;
}
.background-overlay {
  background: rgba(0, 0, 0, 0.45);
}
</style>
