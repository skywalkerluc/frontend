<template>
  <div class="topbar">
    <slot/>
  </div>
</template>
<script>
export default {

}
</script>
<style lang="scss" scoped>
.topbar {
  width: 100%;
  min-height: 300px;
  display: flex;
  background-color: orangered;
  box-shadow: 0px 9px 39px 0px rgba(0,0,0,0.35);
}
</style>


