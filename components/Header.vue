<template>
  <div>
    <header :class="isOpen ? `lg:w-80 w-60 bg-${$store.state.theme.background}-700` : `w-16 bg-${$store.state.theme.background}-700`" class="z-20 py-3 px-3 fixed bg- min-h-full left-0  transition-all ease-in-out duration-300">
      <div class="flex justify-center" v-if="isClosable">
        <button @click="isOpen = !isOpen" class="text-white text-4xl ">
          <font-awesome-icon v-if="!isOpen" :icon="['fa', 'bars']"/>
          <font-awesome-icon v-else :icon="['fa', 'times']"/>
        </button>
      </div>
      <div class="flex flex-col justify-center items-center text-center">
        <h1 :class="`bolder text-2xl text-${$store.state.theme.primaryfontcolor}`">José Miguel Galván</h1>
        <img class="w-44 rounded-full text-center my-5" src="~/assets/img/profile/main-profile.jpg" alt="Profile Image"/>
        <p :class="`text-${$store.state.theme.primaryfontcolor}`"> Hi my name is José Miguel and I'm Full-Stack Developer, Welcome to my personal webiste 🤭</p>
      </div>
      <div class="flex justify-center items-center my-4 gap-2">
        <MenuSocialNetworkItem url="#" iconclass="github" iconclassprefix="fab"/>
        <MenuSocialNetworkItem url="#" iconclass="linkedin" iconclassprefix="fab"/>
      </div>
      <hr class="border-gray-400">
      <div class="flex flex-col py-2 px-8 items-center text-center">
        <MenuLinkItem url="#" iconclassprefix="fa" iconclass="user">About Me</MenuLinkItem>
        <MenuLinkItem url="#" iconclassprefix="fas" iconclass="laptop-code">Portfolio</MenuLinkItem>
        <MenuLinkItem url="#" iconclassprefix="fas" iconclass="file-alt">Resume</MenuLinkItem>
        <MenuLinkItem url="#" iconclassprefix="fas" iconclass="envelope">Contact me</MenuLinkItem>
        <button :class="`text-${$store.state.theme.primaryfontcolor} my-2 py-2 px-3 bg-${$store.state.theme.background}-800 rounded-md transform transition duration-200 ease-in-out hover:scale-110`"><font-awesome-icon class="mx-2" :icon="['fas', 'paper-plane']"/>Hire me</button>
      </div>
      <div class="fixed bottom-0 lg:w-full w-60">
        <p :class="`text-${$store.state.theme.primaryfontcolor}`">This website is powered with Nuxt.js 💚</p>
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