<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Puffy Delivery"/>
    <PuffyMap></PuffyMap>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';
import PuffyMap from '@components/PuffyMap.vue';
export default {
  name: 'home',
  components: {
    HelloWorld,
    PuffyMap
  },
};
</script>
