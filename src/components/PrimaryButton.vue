<script setup>
const props = defineProps({
  size: String,
  badgeCount: Number
});
</script>

<template>
  <button>
    <div class="icon">
      <slot name="icon"></slot>
    </div>
    <slot></slot>
    <div class="badge">{{ props.badgeCount }}</div>
  </button>
</template>

<style scoped>
  button {
    font-family: Inter, sans-serif;
    display: flex;
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
    border-radius: 8px;
  }

  .icon {
    display: flex;
  }

  .badge {
    display: flex;
  }
</style>
