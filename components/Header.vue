<template>
  <div>
    <header :class="isOpen ? `lg:w-80 w-60 bg-green-500` : `w-16 bg-green-500`" class="z-20 fixed bg- min-h-full left-0  transition-all ease-in-out duration-300">
      <div class="flex justify-center" v-if="isClosable">
        <button @click="isOpen = !isOpen" class="text-white text-4xl ">
          <font-awesome-icon v-if="!isOpen" :icon="['fa', 'bars']"/>
          <font-awesome-icon v-else :icon="['fa', 'times']"/>
        </button>
      </div>
      <div class="flex justify-center items-center my-4 gap-2">
        <MenuSocialNetworkItem url="#" iconclass="github" iconclassprefix="fab"/>
        <MenuSocialNetworkItem url="#" iconclass="linkedin" iconclassprefix="fab"/>
      </div>
    </header>
    <transition enter-class="opacity-0" enter-active-class="ease-out transition-medium" enter-to-class="opacity-100" leave-class="opacity-100" leave-active-class="ease-out transition-medium" leave-to-class="opacity-0">
      <div  @keydown.esc="isOpen = false" v-show="isOpen" class="z-10 fixed inset-0 transition-opacity">
        <div v-if="isClosable" @click="isOpen = false" class="absolute inset-0 bg-black opacity-50" tabindex="0"></div>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: true,
      isClosable:false
    }
  },
}
</script>

<style>

</style>