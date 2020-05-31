<template>
  <nav
    class="flex items-center justify-end sm:justify-between flex-wrap bg-teal-500 p-6"
  >
    <div class="block sm:hidden">
      <button
        class="flex items-center px-3 py-2 border rounded text-teal-200 border-teal-400 hover:text-white hover:border-white"
        @click="isClosed = !isClosed"
      >
        <svg
          class="fill-current h-4 w-4"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <title>Menu</title>
          <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
        </svg>
      </button>
    </div>
    <div class="w-full block flex-grow">
      <div class="text-lg sm:flex" :class="{ hidden: isClosed }">
        <nuxt-link
          to="/"
          class="block lg:inline-block text-teal-200 hover:text-white mr-4"
        >
          Top
        </nuxt-link>
        <nuxt-link
          to="/profile"
          class="block lg:inline-block text-teal-200 hover:text-white mr-4"
        >
          Profile
        </nuxt-link>
        <nuxt-link
          to="/works"
          class="block lg:inline-block text-teal-200 hover:text-white mr-4"
        >
          Works
        </nuxt-link>
      </div>
    </div>
  </nav>
</template>

<script lang="ts">
import Vue from 'vue';
export default Vue.extend({
  data() {
    return {
      isClosed: true
    };
  }
});
</script>
