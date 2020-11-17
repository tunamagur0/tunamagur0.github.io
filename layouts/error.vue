<template>
  <div class="container">
    <client-only>
      <h1 v-if="error.statusCode === 404">ページが見つかりません</h1>
      <h1 v-else>エラーが発生しました</h1>
    </client-only>
  </div>
</template>
<script lang="ts">
import Vue from 'vue';
export default Vue.extend({
  props: {
    error: {
      type: Object,
      default: null
    }
  },
  layout: 'default'
});
</script>
