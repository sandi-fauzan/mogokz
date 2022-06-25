<template>
  <header class="flex w-full px-16 py-5 justify-between uppercase">
    <div class="nav-link">
      <router-link class="pr-10 text-gray-600 text-sm hover:text-black" to="/"
        >Home</router-link
      >

      <!-- Dropdown toggle button -->
      <button
        @click="show = !show"
        class="pr-10 text-gray-600 text-sm hover:text-black"
      >
        <span>SHOP</span>

        <font-awesome-icon class="pl-1" icon="angle-down" />
      </button>

      <!-- Dropdown menu -->
      <div
        v-show="show"
        class="
          absolute
          z-40
          lg:ml-16
          py-2
          mt-6
          bg-white
          rounded-md
          shadow-xl
          w-44
        "
      >
        <router-link
          to="/"
          class="
            block
            px-4
            py-4
            text-sm text-gray-500
            hover:bg-gray-100 hover:text-gray-700
          "
        >
          T-Shirt
        </router-link>
        <router-link
          to="/"
          class="
            block
            px-4
            py-4
            text-sm text-gray-500
            hover:bg-gray-100 hover:text-gray-700
          "
        >
          Hoodie
        </router-link>
        <router-link
          to="/"
          class="
            block
            px-4
            py-4
            text-sm text-gray-500
            hover:bg-gray-100 hover:text-gray-700
          "
        >
          Hat
        </router-link>
      </div>

      <router-link
        class="pr-10 text-gray-600 text-sm hover:text-black"
        to="/news"
        >News</router-link
      >
    </div>
    <div class="brand">
      <h1 class="text-3xl text-black font-extrabold">Mogoks.co</h1>
    </div>
    <div class="nav-link">
      <font-awesome-icon class="pl-10" icon="magnifying-glass" />
      <router-link class="pl-10 text-gray-600 text-sm hover:text-black" to="/"
        >Login/Register</router-link
      >
      <router-link
        class="pl-10 text-gray-600 text-sm hover:text-black"
        to="/shop"
        >Wishlist</router-link
      >
      <button class="hover:opacity-70" @click="showSidebar = !showSidebar">
        <font-awesome-icon class="pl-10" icon="cart-shopping" /><span
          class="font-semibold text-xl ml-2"
          >({{ counter }})</span
        >
      </button>

      <!-- Dropdown menu -->
      <div
        v-show="showSidebar"
        class="
          absolute
          z-40
          right-0
          py-2
          mt-6
          bg-white
          rounded-md
          shadow-xl
          w-72
        "
      >
        <div
          class="
            block
            px-4
            py-8
            text-sm text-gray-500
            hover:bg-gray-100 hover:text-gray-700
          "
        >
          <div class="flex">
            <img class="w-12 object-cover" />
            <div class="block ml-3">
              <h3 class="uppercase tracking-wider mt-1 font-semibold">ans</h3>
              <h5
                class="
                  uppercase
                  tracking-wider
                  mt-0
                  text-red-600 text-xs
                  font-semibold
                "
              >
                asd
              </h5>
              <div class="flex mt-2">
                <button
                  class="
                    px-3
                    rounded-full
                    border border-gray-600
                    hover:bg-black hover:text-white
                    text-lg
                  "
                >
                  -
                </button>
                <p class="px-3 text-xl">1</p>
                <button
                  class="
                    px-3
                    rounded-full
                    border border-gray-600
                    hover:bg-black hover:text-white
                    text-lg
                  "
                >
                  +
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      show: false,
      showSidebar: false,
    };
  },
};
</script>

<style>
</style>