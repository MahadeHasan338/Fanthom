<template>
  <transition name="modal-fade">
    <div
      class="fixed top-0 bottom-0 right-0 left-0 z-[999] flex justify-center background-overlay"
      @click="$emit('close-modal')"
    >
      <div class="grid content-center m-10 sm:m-0">
        <div
          class="cursor-pointer flex justify-between items-center py-5"
          @click="$emit('close-modal')"
        ></div>

        <!-- Modal body -->
        <div
          class="text-center modal-bg rounded-md w-[19rem] sm:w-[22.3rem] h-[27rem] sm:h-[28rem] overflow-y-auto no-scrollbar"
          @click.stop
        >
          <div class="fixed modal-bg p-3 rounded-md">
            <input
            type="text"
            class=" py-2.5 pl-2 pr-[4.7rem] sm:pr-32 bg-transparent rounded-md border-[1px] border-gray opacity-70 placeholder:text-lg focus:outline-2 placeholder:font-medium mb-2"
            placeholder="Search in 5180 token"
            v-model="networkName"
          />
          <p class="pt-4 text-left">Assets</p>
          </div >
          <div class="mt-28 p-3">
            <div v-for="asset in assets" :key="asset.id">
            <div class="flex justify-between items-center mb-3">
              <div class="text-left flex">
                <img class="w-10 mr-2" :src="asset.image" alt="" />
                <div>
                  <p>{{ asset.textOne }}</p>
                  <p class="text-[10px]">{{ asset.textTwo }}</p>
                </div>
              </div>
              <div>
                <p>0</p>
              </div>
            </div>
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
      assets: [
        {
          id: 1,
          image: require("../../assets/icon/dex/eth-0/ETH.png"),
          textOne: "ETH(ETH)",
          textTwo: "Ethereum",
        },
        {
          id: 2,
          image: require("../../assets/icon/dex/eth-0/USDT.png"),
          textOne: "USDT(ETH)",
          textTwo: "TetherUSD",
        },
        {
          id: 3,
          image: require("../../assets/icon/dex/eth-0/USDC.png"),
          textOne: "USDC(ETH)",
          textTwo: "USDcoin",
        },
        {
          id: 4,
          image: require("../../assets/icon/dex/eth-0/BUSD.png"),
          textOne: "BUSD(ETH)",
          textTwo: "BinanceUSD",
        },
        {
          id: 5,
          image: require("../../assets/icon/dex/eth-0/DAI.png"),
          textOne: "DAI(ETH)",
          textTwo: "DaiStablecoin",
        },
        {
          id: 6,
          image: require("../../assets/icon/dex/eth-0/TRX.jpg"),
          textOne: "TRX(ETH)",
          textTwo: "TRON",
        },
        {
          id: 7,
          image: require("../../assets/icon/dex/eth-0/SHIB.png"),
          textOne: "SHIB(ETH)",
          textTwo: "",
        },
        {
          id: 7,
          image: require("../../assets/icon/dex/eth-0/SHIB.png"),
          textOne: "SHIB(ETH)",
          textTwo: "",
        },
        {
          id: 7,
          image: require("../../assets/icon/dex/eth-0/SHIB.png"),
          textOne: "SHIB(ETH)",
          textTwo: "",
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
