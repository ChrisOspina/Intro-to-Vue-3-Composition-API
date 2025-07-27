<script setup>
 import { ref } from 'vue';
 import socksGreenImage from './assets/images/socks_green.jpeg'

 const product = ref('Socks');
 const image = ref(socksGreenImage)
 const inventory = ref(100)
 const onSale = ref(TextTrackCue)

 const description = ref('Just some new socks on sale');
</script>

<template>
<div class="nav-bar"></div>
<div class="product-display">
  <div class="product-container">
    <div class="product-image">
      <img v-bind:src="image"/>
    </div>
    <div class="product-info">
      <h1>{{ product }}</h1>
      <p v-if="inventory > 10">In stock</p>
      <p v-else-if="inventory <=10  && inventory > 0">Almost sold out</p>
      <p v-else>Out of stock</p>
      <br/>
      <p v-if="onSale"><strong>On Sale</strong></p>
    </div>
  </div>
</div>
</template>
