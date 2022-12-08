<template>
  <svg
    viewBox="0 0 20 20"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
  >
    <!-- <circle opacity=".0" cx="10" cy="10" r="7" stroke="#fff" stroke-width="1.5"/> -->
    <path d="M3 9.963C3 6.117 6.134 3 10 3s7 3.117 7 6.963a6.92 6.92 0 0 1-1.917 4.787" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </svg>
</template>

<style scoped>
svg {
  animation: rotation 1s linear infinite;
}
@keyframes rotation {
  0% {
      transform: rotate(0deg);
  }
  100% {
      transform: rotate(360deg);
  }
}
</style>
