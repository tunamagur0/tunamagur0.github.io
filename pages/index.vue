<template>
  <div
    class="min-h-screen flex justify-center items-center text-center bg-gray-600"
  >
    <div class="flex justify-center">
      <div class="w-1/3 mx-10 relative">
        <p class="absolute text-3xl z-10">Profile</p>
        <nuxt-link to="profile">
          <img class="blur-img" src="~/assets/img/profile.png" alt="works" />
        </nuxt-link>
      </div>
      <div class="w-1/3 mx-10 relative">
        <p class="absolute text-3xl z-10">Works</p>
        <nuxt-link to="works">
          <img class="blur-img" src="~/assets/img/works.png" alt="works" />
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  layout() {
    return 'headerNone';
  }
});
</script>

<style scoped>
.blur-img {
  filter: blur(0.5rem);
}

.blur-img:hover {
  filter: blur(0.04rem);
}
</style>
