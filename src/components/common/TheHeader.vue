<template>
  <section
    class="
      grid
      justify-end
      sticky
      z-10
      top-0
      bg-[#2D3541]
      pt-3
      pb-5
      sm:py-5
      px-0
    "
  >
    <div>
      <ul class="flex">
        <li class="relative group">
          <a href="#" class="button-style box-shadow px-2 sm:px-3"
            ><img
              class="w-5 h-5 mr-0 sm:mr-2"
              src="../../assets/icon/header/1.svg"
              alt=""
            />
            <span class="hidden sm:block"> Fantom</span></a
          >

          <ul
            class="
              opacity-0
              group-hover:opacity-100
              transition-all
              duration-300
              ease-linear
            "
          >
            <li
              class="
                absolute
                -left-3
                top-12
                bg-[rgba(60,67,78,1)]
                pt-4
                pb-8
                px-2
                rounded-md
                box-shadow
              "
            >
              <a
                href="#"
                class="
                  flex
                  items-center
                  text-white
                  hover:bg-[#555B64]
                  pr-16
                  pl-3
                  py-2
                  rounded-md
                  transition-all
                  duration-100
                  ease-linear
                "
                ><img
                  class="w-5 h-5 mr-2"
                  src="../../assets/icon/header/3.svg"
                  alt=""
                />Moonriver</a
              >
            </li>
          </ul>
        </li>

        <li class="relative group">
          <a href="#" class="button-style box-shadow px-3"
            ><img
              class="w-5 h-5 mr-2"
              src="../../assets/icon/header/2.svg"
              alt=""
            />FHM</a
          >

          <ul
            class="
              opacity-0
              group-hover:opacity-100
              transition-all
              duration-300
              ease-linear
              absolute
              -left-20
              top-12
              bg-[rgba(60,67,78,1)]
              p-3
              rounded-md
              box-shadow
            "
          >
            <p class="text-[13px] mb-1">ADD TOKEN TO WALLET</p>
            <li class="flex justify-center items-center gap-x-1 text-[13px]">
              <a
                href="#"
                class="
                  text-white
                  hover:bg-[#555B64]
                  py-1
                  px-4
                  rounded-md
                  transition-all
                  duration-100
                  ease-linear
                  text-center
                "
              >
                <img
                  class="w-7 mb-1 inline"
                  src="../../assets/icon/fhm/1.png"
                  alt=""
                />
                USDB</a
              >
              <a
                href="#"
                class="
                  text-white
                  hover:bg-[#555B64]
                  py-1
                  px-4
                  rounded-md
                  transition-all
                  duration-100
                  ease-linear
                  text-center
                "
              >
                <img
                  class="w-7 mb-1 inline"
                  src="../../assets/icon/fhm/2.svg"
                  alt=""
                />
                FHM</a
              >
              <a
                href="#"
                class="
                  text-white
                  hover:bg-[#555B64]
                  py-1
                  px-4
                  rounded-md
                  transition-all
                  duration-100
                  ease-linear
                  text-center
                "
              >
                <img
                  class="w-7 mb-1 inline"
                  src="../../assets/icon/fhm/3.svg"
                  alt=""
                />
                sFHM</a
              >
              <a
                href="#"
                class="
                  text-white
                  hover:bg-[#555B64]
                  py-1
                  px-4
                  rounded-md
                  transition-all
                  duration-100
                  ease-linear
                  text-center
                "
              >
                <img
                  class="w-7 mb-1 inline"
                  src="../../assets/icon/fhm/4.svg"
                  alt=""
                />
                fwsFHM</a
              >
            </li>
          </ul>
        </li>

        <li>
          <a
            href="#"
            @click="$emit('show-the-modal')"
            class="px-5 button-style box-shadow"
            >Connect Wallet</a
          >
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      showWalletModal: false,
    };
  },
};
</script>

<style scoped>
.background {
  background: linear-gradient(180deg, #313945, #161d26);
}
.button-style {
  @apply py-2 bg-[rgba(60,67,78,0.4)] flex items-center  rounded-md shadow-lg mr-2 sm:mr-3 text-white text-[15px] hover:bg-[#4E555E] transition-all duration-100 ease-linear;
}
</style>
