<template>
  <div>
    <!-- Google Tag Manager (noscript) -->
    <!-- <noscript
      ><iframe
        src="https://www.googletagmanager.com/ns.html?id=GTM-M6RBR2ZZ"
        height="0"
        width="0"
        style="display: none; visibility: hidden"
      ></iframe
    ></noscript> -->
    <!-- End Google Tag Manager (noscript) -->
    <div class="data_display">GTM FIRST V_{{ version }}</div>
    <div class="triggers">
      <button @click="triggerCustom">Custom Event</button>
      <button @click="addToCart">Add To Cart</button>
    </div>
  </div>
</template>
<script setup>
import { version } from "../package.json";
const triggerCustom = () => {
  gtag("");
};

const addToCart = () => {
  gtag("event", "add_to_cart", {
    currency: "USD",
    value: 30.03,
    items: [
      {
        item_id: "SKU_12345",
        item_name: "Stan and Friends Tee",
        affiliation: "Google Merchandise Store",
        coupon: "SUMMER_FUN",
        discount: 2.22,
        index: 0,
        item_brand: "Google",
        item_category: "Apparel",
        item_category2: "Adult",
        item_category3: "Shirts",
        item_category4: "Crew",
        item_category5: "Short sleeve",
        item_list_id: "related_products",
        item_list_name: "Related Products",
        item_variant: "green",
        location_id: "ChIJIQBpAG2ahYAR_6128GcTUEo",
        price: 10.01,
        quantity: 3,
      },
    ],
  });
};
</script>
<style>
.triggers {
  flex: auto;
  margin-top: 40px;
  align-items: center;
  justify-items: center;
}
.triggers button {
  padding: 4px;
  font-weight: 600px;
  margin: 5px;
}
</style>
