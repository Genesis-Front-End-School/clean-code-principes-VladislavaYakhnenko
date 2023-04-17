<template>
  <div class="flex items-center gap-1.5">
    <span class="font-montserrat font-semibold text-gray-500 text-xl max-lg:text-lg max-md:text-base">
      {{ rating }}
    </span>
    <StarIcon/>
  </div>
</template>

<script setup>
import StarIcon from "@/components/icons/StarIcon.vue";
import {computed} from "vue";

const props = defineProps({
  rating: {
    type: Number,
    required: true,
  }
})

const rating = computed(() => {
  return props.rating.toFixed(1);
})
</script>

<style scoped>

</style>