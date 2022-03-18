<template>
  <div>
      <div class="flex flex-col">
        <div class="flex">
            <font-awesome-icon v-for="icon in icons" :key="icon.class" :class="`text-${icon.color} text-3xl  ml-2`" :icon="[icon.prefix, icon.class]"/>
        </div>
        <p class="text-justify text-md font-bold">
            <slot></slot>
        </p>
        <p class="text-justify text-md">
            <slot name="resume"></slot>
        </p>
      </div>
  </div>
</template>

<script>
export default {
    props: {
        icons: {
            type: Array
        },
    },
}
</script>

<style>

</style>