<template>
  <div class="home relative">
    <div class="img">
      <div class="btn absolute block w-full text-center">
        <router-link
          to="/shop"
          class="
            inline-block
            px-44
            py-6
            bg-black
            font-semibold
            text-white
            shadow-md
            transform
            transition
            ease-in-out
            hover:translate-y-2 hover:opacity-90
          "
          >EXPLORE NOW</router-link
        >
      </div>
    </div>

    <Shirt />
    <Hoodie />
  </div>
</template>

<script>
import Shirt from "@/views/products/Shirt.vue";
import Hoodie from "@/views/products/Hoodie.vue";

export default {
  name: "Home",
  components: {
    Shirt,
    Hoodie,
  },
};
</script>

<style scoped>
.home {
  position: relative;
  width: 100%;
  height: 660px;
}
.img {
  position: relative;
  width: 100%;
  height: 660px;
  background-image: url(https://images.unsplash.com/photo-1508427953056-b00b8d78ebf5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80);
  background-repeat: no-repeat;
  background-size: cover;
  filter: brightness(70%) grayscale(70%);
}

.btn {
  margin-top: 520px;
}
</style>
