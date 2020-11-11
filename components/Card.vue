<template>
  <div class="max-w-sm rounded overflow-hidden shadow-lg m-6">
    <div class="flex justify-center p-2 hover:shadow-md">
      <slot name="image" />
    </div>
    <div class="px-6 py-4">
      <div class="font-bold text-xl mb-2"><slot name="title" /></div>
      <div class="text-gray-700 text-base">
        <slot name="content" />
      </div>
    </div>
    <div class="flex px-6 py-4">
      <slot name="icons" />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
export default Vue.extend({
  name: 'Card'
});
</script>
