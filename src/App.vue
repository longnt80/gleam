<script setup>
import PrimaryButton from "./components/PrimaryButton.vue";
import IconPlus from "./components/icons/IconPlus.vue";
</script>

<template>
  <main>
    <div>
      <!-- Default button -->
      <PrimaryButton>
        Button
      </PrimaryButton>

      <!-- With icon -->
      <PrimaryButton>
        <template #icon><IconPlus /></template>
        Button
      </PrimaryButton>

      <PrimaryButton>
        <template #icon><IconPlus /></template>
      </PrimaryButton>

      <PrimaryButton :badge-count="3">
        Button
      </PrimaryButton>

      <PrimaryButton :badge-count="3">
        <template #icon><IconPlus /></template>
        Button
      </PrimaryButton>

      <PrimaryButton :badge-count="3" :is-loading="true">
        <template #icon><IconPlus /></template>
        Button
      </PrimaryButton>

      <PrimaryButton :badge-count="3">
        <template #icon><IconPlus /></template>
      </PrimaryButton>

      <PrimaryButton :disabled="true" :badge-count="3">
        <template #icon><IconPlus /></template>
        Button
      </PrimaryButton>
    </div>

    <div>
      <!-- Default button -->
      <PrimaryButton :is-loading="true">
        Button
      </PrimaryButton>

      <!-- With icon -->
      <PrimaryButton :is-loading="true">
        <template #icon><IconPlus /></template>
        Button
      </PrimaryButton>

      <PrimaryButton :is-loading="true">
        <template #icon><IconPlus /></template>
      </PrimaryButton>

      <PrimaryButton :badge-count="3" :is-loading="true">
        Button
      </PrimaryButton>

      <PrimaryButton :badge-count="3" :is-loading="true">
        <template #icon><IconPlus /></template>
        Button
      </PrimaryButton>

      <PrimaryButton :badge-count="3" :is-loading="true">
        <template #icon><IconPlus /></template>
      </PrimaryButton>

      <PrimaryButton :disabled="true" :badge-count="3" :is-loading="true">
        <template #icon><IconPlus /></template>
        Button
      </PrimaryButton>
    </div>
  </main>
</template>

<style scoped>
main {
  display: flex;
  gap: 20px;
}

main > div {
  display: flex;
  gap: 10px;
  flex-direction: column;
  align-items: flex-start;
}
</style>
