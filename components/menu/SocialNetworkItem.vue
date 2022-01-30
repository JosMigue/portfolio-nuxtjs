<template>
  <div>
    <a :href="url" :class="`bg-white rounded-full py-1 px-2 text-${$store.state.theme.iconcolor}-500`">
      <font-awesome-icon :icon="[iconclassprefix, iconclass]"/>
    </a>
  </div>
</template>

<script>
export default {
    data() {
        return {
            
        }
    },
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
            default: 'react'
        },
    },
}
</script>

<style>

</style>