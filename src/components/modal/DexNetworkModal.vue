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
        background-overlay
      "
      @click="$emit('close-modal')"
    >
      <div class="grid content-center m-10 sm:m-0">
        <div
          class="cursor-pointer flex justify-between items-center py-5"
          @click="$emit('close-modal')"
        ></div>

        <!-- Modal body -->
        <div
          class="
            text-center
            modal-bg
            rounded-md
            w-[19rem]
            sm:w-[18rem]
            h-[33rem]
            overflow-y-auto
            no-scrollbar
            p-4
          "
          @click.stop
        >
          <p class="text-left text-2xl mb-2">Select Network</p>
          <div
            class="flex justify-center"
            v-for="network in networks"
            :key="network.id"
          >
            <div class="flex items-center">
              <img class="w-10 mr-6 my-3" :src="network.image" alt="" />
              <p class="text-lg">{{ network.text }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  emits: ["close-modal"],
  data() {
    return {
      networkName: "",
      checked: true,
      networks: [
        {
          id: 1,
          image: require("../../assets/icon/dex/eth/eth.svg"),
          text: "ETH",
        },
        {
          id: 2,
          image: require("../../assets/icon/dex/eth/bsc.svg"),
          text: "BSC",
        },
        {
          id: 3,
          image: require("../../assets/icon/dex/eth/fantom.svg"),
          text: "FANTOM",
        },
        {
          id: 4,
          image: require("../../assets/icon/dex/eth/arbitrum.svg"),
          text: "ARBITRUM",
        },
        {
          id: 5,
          image: require("../../assets/icon/dex/eth/AVALANCHE.svg"),
          text: "AVALANCHE",
        },
        {
          id: 6,
          image: require("../../assets/icon/dex/eth/HARMONY.svg"),
          text: "HARMONY",
        },
        {
          id: 6,
          image: require("../../assets/icon/dex/eth/POLYGON.svg"),
          text: "POLYGON",
        },
      ],
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
  background: rgba(0, 0, 0, 0.5);
}
.modal-bg {
  background-color: rgb(30, 38, 48);
}
</style>
