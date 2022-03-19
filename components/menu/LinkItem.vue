<template>
      <NuxtLink :to="url" :class="`w-full rounded-lg transform trasition-all duration-200 ease-in-out font-bold hover:bg-${$store.state.theme.background}-500 py-4 block text-${$store.state.theme.primaryfontcolor}`">
        <font-awesome-icon class="mx-2" :icon="[iconclassprefix, iconclass]"/><slot></slot>
      </NuxtLink>
</template>

<script>
export default {
    props: {
        url: {
            type: String,
            default: '#'
        },
        iconclassprefix:{
            type: String,
            default: 'fab'
        },
        iconclass: {
            type: String,
            default: 'vuejs'
        },
    },
}
</script>

<style>

</style>