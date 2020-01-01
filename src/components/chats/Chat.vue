<template>
  <div>
    <div
      class="flex px-4 py-2 hover:bg-dark rounded cp"
      v-for="i in [1,2,3,4,5,6,7,8,9,0,'a','b','c','d','e']"
      :key="i"
    >
      <img :src="user.avatar" class="w-12 h-12 rounded-full" alt />
      <div class="px-4">
        <h3>{{ user.name }}</h3>
        <p class="text-sm text-placeholder">Lorem ipsum dolor sit amet.</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["user"]
};
</script>
