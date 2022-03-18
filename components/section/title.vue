<template>
  <div>
    <h2 class="section-title font-bold text-3xl"><slot></slot></h2>
  </div>
</template>

<script>
export default {

}
</script>

<style>
  .section-title{
    font-size: 2rem;
    position: relative;
    padding-left: 1.5rem;
  }
 .section-title:before{
   content: "";
   background-color: rgb(29 78 216);
   width: 5px;
   height: 100%;
   display: inline-block;
   position: absolute;
   left: 0;
   top: 0;
 }
</style>