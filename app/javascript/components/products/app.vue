<template>
  <div>
    <AppLinks></AppLinks>
    <router-view
      :products="products"
      :products_ranking="products_ranking"
      :products_likescounts="products_likescounts"
    ></router-view>
  </div>
</template>
<script>
import AppLinks from "./AppLinks.vue";
import CreatedAtDesc from "./CreatedAtDesc.vue";
import FavorDesc from "./FavorDesc.vue";

export default {
  name: "App",
  components: {
    AppLinks,
    CreatedAtDesc,
    FavorDesc,
  },
  props: {
    products: {
      type: Array,
      default: () => "",
    },
    products_ranking: {
      type: Array,
      default: () => "",
    },
    products_likescounts: {
      type: Object,
      default: () => "",
    },
  },
};
</script>
