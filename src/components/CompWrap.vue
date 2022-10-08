<template>
  <section class="px-3 sm:px-5">
    <div class="grid grid-cols-7 sm:my-3 ">
      <div class="xl:col-span-1"></div>
      <div class="col-span-7 xl:col-span-5 main-info lg:ml-7 xl:mx-7">
        <div>
          <h4 class="text-[18px] text-h5 py-0">Wrap / Unwrap</h4>
        </div>

        <div class="flex flex-col sm:flex-row sm:justify-evenly pt-10 sm:py-10">
          <div class="text-start sm:text-center">
            <h4 class="text-h4 text-gray">sFHM Price</h4>
            <h4 class="text-h4">$1.04</h4>
          </div>
          <div class="text-start sm:text-center pt-4 sm:pt-0">
            <h4 class="text-h4 text-gray">Current Index</h4>
            <h4 class="text-h4">73.65 FHM</h4>
          </div>
          <div class="text-start sm:text-center pt-4 sm:pt-0">
            <h4 class="text-h4 text-gray">fwsFHM</h4>
            <h4 class="text-h4">$76.38</h4>
          </div>
        </div>

        <div class="text-center mt-5 sm:mt-0">
          <a href="#" @click="$emit('show-the-modal')" class="wallet-button"
            >Connect Wallet</a
          >
        </div>

        <p class="text-center mt-5">Connect your wallet to stake FHM</p>
      </div>
      <div class="xl:col-span-1"></div>
    </div>
  </section>
</template>

<style scoped>
.text-h4 {
  @apply text-[1.3rem] font-normal;
}
</style>
