<template>
  <div
    @click="toggleAccordion"
    class="as-accordion__header"
    :class="{ 'as-accordion__header--open': visible() }"
  >
    <slot />
    <i
      class="as-icon-blue"
      :class="{
        'as-icon-arrow-top': visible(),
        'as-icon-arrow-down': !visible(),
      }"
    ></i>
  </div>
</template>

<script setup>
import { inject } from "vue";

const visible = inject("visible");
const toggleAccordion = inject("toggleAccordion");
</script>
