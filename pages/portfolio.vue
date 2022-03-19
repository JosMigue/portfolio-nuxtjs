<template>
  <div>
    Portfolio Page
  </div>
</template>

<script>
export default {
  transition: 'home'
}
</script>

<style>
.home-enter { transform: translateX(100%) }
.home-enter-to { transform: translateX(0) }
.home-enter-active { position: absolute }

.home-leave { transform: translateX(0) }
.home-leave-to { transform: translateX(-100%) }

.home-enter-active,
.home-leave-active { transition: all 750ms ease-in-out }
</style>