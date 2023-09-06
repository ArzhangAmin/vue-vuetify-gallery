<script setup>
  import SideBar from "./components/SideBar.vue";
  import ImageGallery from "./components/ImageGallery.vue";
  import {ref} from "vue";

  const isWithColor = ref(true);
  
  const onSelectOption = (isColor) => {
    isWithColor.value = isColor;
  }
</script>
 
<template>
  <v-app>
    <!--SIDEBAR-->
    <SideBar @selectOption="onSelectOption"></SideBar>
    <v-main>
      <!--CARDS-->
      <image-gallery :isWithColor="isWithColor"></image-gallery>
    </v-main>
  </v-app>
</template>

