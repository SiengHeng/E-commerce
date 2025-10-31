<script setup lang="ts">
import Button from './Button.vue';

const props = defineProps<{
  text: string;
  color: string;
  pic: string;
  btncolor: string;
}>();
</script>

<template>
  <div
    class="relative flex justify-between items-center rounded-xl p-6 w-[420px] h-[220px] shadow hover:shadow-lg transition"
    :style="{ backgroundColor: props.color }"
  >
    <!-- Left: Text and Button -->
    <div class="flex flex-col items-start justify-center gap-3 z-10 w-1/2">
      <h1 class="text-gray-800 font-bold text-lg leading-snug">
        {{ props.text }}
      </h1>
      <Button :btncolor="props.btncolor" />
    </div>

    <!-- Right: Image -->
    <img
      :src="props.pic"
      alt="pic"
      class="absolute bottom-0 right-4 h-3/4 object-contain"
    />
  </div>
</template>
