<script setup>
import IconDiamond from './icons/IconDiamond.vue';
import IconLoading from './icons/IconLoading.vue';

const props = defineProps({
  size: String,
  badgeCount: Number,
  disabled: Boolean,
  isLoading: Boolean,
});

console.log(props)
</script>

<template>
  <button :disabled="props.disabled">
    <div class="icon">
      <slot name="icon"></slot>
    </div>
    <slot></slot>
    <div v-if="props.badgeCount" class="badge">
      <IconDiamond class="badge-icon" />
      {{ props.badgeCount }}
    </div>
    <div v-if="props.isLoading" class="loader"><IconLoading /></div>
  </button>
</template>

<style scoped>
  button {
    font-family: Inter, sans-serif;
    display: inline-flex;
    gap: 12px;
    justify-content: center;
    align-items: center;
    height: 40px;
    font-size: 13px;
    padding: 10px;
    line-height: 20px;
    font-weight: 500;
    color: #fff;
    background: #33B679;
    border: none;
    box-shadow: 0px 2px 4px rgba(10, 14, 20, 0.08);
    border-radius: 8px;
  }

  button:hover {
    background: linear-gradient(0deg, rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.2)), #33B679;
  }

  button:active {
    background: linear-gradient(0deg, rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)), #33B679;
  }

  button:disabled {
    background: linear-gradient(0deg, rgba(255, 255, 255, 0.6), rgba(255, 255, 255, 0.6)), #33B679;
    cursor: not-allowed;
  }

  button:focus-visible {
    outline: none;
    box-shadow: 0px 0px 0px 3px rgb(255,255,255), 0px 0px   0px 4px rgba(51,182,121,0.6);
  }

  .icon {
    display: flex;
    width: 20px;
    height: 20px;
  }

  .icon:empty {
    display: none;
  }

  .badge {
    display: flex;
    gap: 4px;
    justify-content: center;
    align-items: center;
    background-color: rgba(255, 255, 255, 0.12);
    border-radius: 100px;
    padding: 4px 8px;
    font-size: 12px;
    height: 24px;
    width: 44px;
  }

  .badge .badge-icon {
    width: 16px;
    height: 16px;
  }

  .loader {
    width: 20px;
    height: 20px;
    color: #fff;
  }
</style>
