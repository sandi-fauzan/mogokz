<template>
  <h1 class="px-60 pt-32 text-3xl pb-16 font-semibold">New Hoodie</h1>
  <div class="shirt grid grid-cols-3 gap-6 px-60 pb-36">
    <div
      class="card w-full overflow-hidden"
      v-for="item in hoodie"
      :key="item.id"
      :item="item"
    >
      <div class="w-full group">
        <div
          class="
            absolute
            cursor-pointer
            bg-gray-200
            px-3
            py-2
            rounded-full
            mr-auto
            m-2
            group-hover:bg-red-50
            transition
            duration-500
          "
        >
          <!-- <button @click="addToCart()">
            <font-awesome-icon
              class="
                mt-2
                ml-auto
                text-gray-400
                transition
                duration-500
                group-hover:text-red-300
                focus:text-red-500
              "
              icon="cart-shopping"
            />
          </button> -->
          <button @click="tambah()">
            <font-awesome-icon
              class="
                mt-2
                ml-auto
                text-gray-400
                transition
                duration-500
                group-hover:text-red-300
                focus:text-red-500
              "
              icon="cart-shopping"
            />
          </button>
        </div>
      </div>
      <img
        class="transition ease-in-out"
        :src="item.imgUrl"
        :alt="item.title"
      />
      <div class="card-body text-center">
        <h3
          class="cursor-pointer hover:underline font-semibold text-xl pt-3 pb-1"
        >
          {{ item.title }}
        </h3>
        <h4 class="font-bold text-red-600">
          <span class="text-gray-400 font-medium text-xs line-through"
            >Rp. {{ item.diskon }}</span
          >
          Rp. {{ item.price }}
        </h4>
      </div>
    </div>
  </div>
</template>

<script>
import hoodie from "@/mock/hoodie.json";
export default {
  props: ["item"],
  data() {
    return {
      hoodie,
    };
  },
  methods: {
    addToCart() {
      this.$store.commit("addToCart", this.item);
    },
    
  },
  computed: {
    product_total() {
      return this.$store.getters.productQuantity(this.item);
    },
  },
};
</script>

<style>
.card img {
  width: 100%;
  max-height: 386px;
  background-repeat: no-repeat;
  background-size: cover;
  overflow: hidden;
}
</style>